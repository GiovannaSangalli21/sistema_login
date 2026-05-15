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

#5. Configuração de Serviços e Acesso Remoto
O que fizemos: Instalamos as ferramentas (openssh) no Ubuntu para conseguir mexer no servidor de longe e mandar arquivos com segurança.
Status: O serviço já está ligado e funcionando perfeitamente (active).
Conexão: Ele está pronto para receber visitas pela porta 22, que é o padrão de segurança.

Conexão: Ele está pronto para receber visitas pela porta 22, que é o padrão de segurança.
<img width="1219" height="724" alt="image" src="https://github.com/user-attachments/assets/85bfa900-8ff0-47a4-97e1-7ad0fcd99d56" />
<img width="1218" height="738" alt="image" src="https://github.com/user-attachments/assets/ac36072a-436d-4348-91fe-f178b9eeb465" />
<img width="1221" height="723" alt="image" src="https://github.com/user-attachments/assets/90886247-0247-4dc6-9ff5-add07a332426" />













