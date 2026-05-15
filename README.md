# 🖥️ Serviços de redes - Aplicação Full-Stack

# 1. Configuração do Ambiente de Virtualização
Aqui são as configurações da maquina, que ficou identificada como VM_ubundo

<img width="398" height="192" alt="Captura de tela 2026-04-24 102400" src="https://github.com/user-attachments/assets/6e16c172-2869-47ab-a503-67dd9a93dfc6" />

# 2. Instalação do Sistema Operacional
O sistema Ubuntu 24.04.4 LTS foi selecionado para o projeto, com a instalação já iniciada. A rede foi configurada via cabo para melhorar a integridade dos pacotes adicionais e a verificação de drivers. Até aqui , o processo encontra na fase de escrita de arquivos no disco.

<img width="958" height="817" alt="Captura de tela 2026-04-24 094247" src="https://github.com/user-attachments/assets/ac6f3d4a-bf04-479f-b0dd-eaa8bdf5e62e" />

# 3. Preparação de Ferramentas de Transferência (Host)
- O que foi feito: Instalamos o FileZilla Client no computador (Windows 64 bits).

- Para que serve: Ele será o nosso "gerenciador de arquivos" para o serviço de FTP.

- Na prática: É com ele que vamos enviar e receber arquivos entre o nosso PC e o servidor de um jeito fácil e organizado, conforme pede o exercício.

<img width="1180" height="585" alt="image" src="https://github.com/user-attachments/assets/a6656167-8563-41c0-8b7e-88592a3e8521" />

# 4. Desenvolvimento da Aplicação Web (Serviço HTTP)

Tecnologia: Backend desenvolvido em Python com o framework Flask.

Rede: Servidor ativo no IP 0.0.0.0 (aberto para a rede) na porta 8000.

Segurança: Rota /login com autenticação de usuário e senha específicos.

Feedback: como resposta rapida se foi com susseso ou deu erro.

<img width="497" height="480" alt="image" src="https://github.com/user-attachments/assets/41a6c24e-9393-452c-932f-29f6dd0e8e56" />

<img width="1054" height="565" alt="image" src="https://github.com/user-attachments/assets/972f99bb-0cf7-418b-92d7-c0767a8c859e" /> 

Aqui foi os codigos que utilizamos para centralizar a tela, e a cor

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/5be31e8f-a225-4d02-bd73-003491e6c196" />

Aqui foi para criar o usuario e a senha 

# 5. Configuração de Serviços e Acesso Remoto
O que fizemos: Instalamos as ferramentas (openssh) no Ubuntu para conseguir mexer no servidor de longe e mandar arquivos com segurança.
Status: O serviço já está ligado e funcionando perfeitamente (active).
Conexão: Ele está pronto para receber visitas pela porta 22, que é o padrão de segurança.

Conexão: Ele está pronto para receber visitas pela porta 22, que é o padrão de segurança.
<img width="1219" height="724" alt="image" src="https://github.com/user-attachments/assets/85bfa900-8ff0-47a4-97e1-7ad0fcd99d56" />
<img width="1218" height="738" alt="image" src="https://github.com/user-attachments/assets/ac36072a-436d-4348-91fe-f178b9eeb465" />
<img width="1221" height="723" alt="image" src="https://github.com/user-attachments/assets/90886247-0247-4dc6-9ff5-add07a332426" />

# 7 . Execução do Servidor Web (Flask)
- Acesso ao Link: O link gerado foi http://127.0.0.1:8000. Se tentar usar "https" (com S) agora, vai dar erro porque ainda não configuramos certificados de segurança. O acesso padrão é via HTTP.

- Ajuste no Ambiente (venv): O Flask foi instalado direto no sistema (via sudo apt), mas o projeto já tem uma pasta venv. O ideal é ativar esse ambiente e instalar as coisas lá dentro para o projeto ficar organizado e não depender de permissões de administrador (sudo) toda hora.

- Visibilidade na Rede: Como configuramos o IP 0.0.0.0, qualquer computador na mesma rede consegue acessar a tela de login. Para isso, basta trocar o "127.0.0.1" pelo IP real da máquina onde o código está rodando.

<img width="497" height="480" alt="Captura de tela 2026-05-15 112659" src="https://github.com/user-attachments/assets/0453dbc1-325b-4b5d-a2c0-f02a5c48be49" />

<img width="1054" height="565" alt="Captura de tela 2026-05-15 112848" src="https://github.com/user-attachments/assets/0ddb75ee-1153-4e43-86d2-542862a1eefb" />

<img width="938" height="519" alt="image" src="https://github.com/user-attachments/assets/60ad7211-f76f-4441-b8b5-8eddb3c16759" />
 com essas informações roda nosso site tanto no windons, tanto no umbundo

# 8. Conectar no do colega
Nesta fase, testamos a aplicação para ver se ela aguentava acessos de outros dispositivos, simulando como o sistema se comporta em um ambiente real.

. Conectividade e Acesso Externo
Identificamos o IP da máquina (10.10.147.164) e validamos que o redirecionamento de portas do VirtualBox está funcionando. Com isso, qualquer pessoa na mesma rede conseguiu acessar o sistema pelo link http://10.10.147.164:8000.

. Interface e Visual
O navegador carregou tudo certinho: o fundo temático e o formulário rosa apareceram sem erros. Isso prova que o Flask está conseguindo entregar os arquivos de estilo (CSS) e as imagens para quem acessa de fora.

. Teste de Login (Backend)
Testamos a lógica de entrada de dados para garantir que o sistema está seguro:

Ação: Digitamos o usuário Giovanna e a senha cadastrada.

Resultado: O formulário enviou os dados para o servidor (via rota /login), que validou as credenciais e respondeu com a mensagem de sucesso.

Conclusão: O sistema está estável, acessível na rede local e com a lógica de login funcionando perfeitamente.

<img width="1202" height="581" alt="image" src="https://github.com/user-attachments/assets/7861828b-3a76-4372-83e5-d079025912b5" />


<img width="1240" height="504" alt="image" src="https://github.com/user-attachments/assets/2cd6a0c5-9ccf-4715-b301-9853e41d6b76" />

<img width="1237" height="788" alt="image" src="https://github.com/user-attachments/assets/a475549e-91cc-4dad-bdb0-5dadb55a19bd" />

<img width="1240" height="760" alt="image" src="https://github.com/user-attachments/assets/b42c80a8-0436-49f2-8faf-f3c8aa2a8f53" />

<img width="1238" height="722" alt="image" src="https://github.com/user-attachments/assets/d848c694-9140-4670-8fae-22c6b625da8f" />

<img width="1240" height="682" alt="image" src="https://github.com/user-attachments/assets/d15c510d-7c61-44ab-a768-85661a098292" />




# 6. Configuração de Serviços e Acesso Remoto
Para permitir a gestão do servidor e a transferência de arquivos via rede, foram configurados protocolos de comunicação segura e regras de redirecionamento no host.

- A Implementação do Servidor SSH/SFTP

- O serviço de acesso remoto foi instalado e validado diretamente no terminal da máquina virtual Ubuntu:

 - Instalação: Foram instalados os pacotes openssh-server e openssh-sftp-server para permitir conexões seguras e transferência de arquivos.

- Status do Serviço: O serviço ssh.service foi devidamente ativado e encontra-se no estado active (running).

- Porta de Escuta: O servidor está configurado para ouvir conexões na porta padrão 22.
(não tinha foto desse processo)

























