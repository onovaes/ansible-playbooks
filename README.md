# Meus Playbooks

Acreditamos que já tenha o ansible instalado na sua maquina.

TODO LIST
- Tirar inventario do playbook, pois devo passar como parametro no docker
- validando instlaco do dockers
- Acredito que não estava fazendo o upgrade inicial automatico

### Ubuntu setup inicial

[initial_setup_ubuntu2004] - Faz as configurações iniciais no ubuntu. Testado no Ubuntu 20.04 LTS

- Atualiza os pacotes
- Desabilita o login em ssh com o usuário root 
- Cria e Adiciona o meu usuário ao grupo whell (Super Usuário)
- Adiciona a minha chave publica ssh ao usuário criado no passo anterior
- Instala alguns pacotes como   'curl', 'vim', 'git', 'ufw','fail2ban'

## 1 - Clonando o repo e entrando na pasta
$git clone git@github.com:onovaes/ansible-playbooks.git
cd ansible-playbooks

## 2 - Editar arquivo de configuração 
$vim ubuntu_initial_setup/vars/default.yml

## 3 - Executar playbook

Executaremos como root na primeira vez.

$ansible-playbook -u root initial_setup_ubuntu2004/playbook.yml 


Leituras importantes-
    https://docs.docker.com/engine/install/linux-postinstall/

