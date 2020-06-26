# Meus Playbooks

Acreditamos que já tenha o ansible instalado na sua maquina. 

TODO LIST
- Setar hostame
- Acredito que não estava fazendo o upgrade inicial automatico

### Ubuntu setup inicial

[ubuntu_initial_setup] - Faz as configurações iniciais no ubuntu. Testado no Ubuntu 20.04 LTS

- Atualiza os pacotes
- Desabilita o login em ssh com root 
- Adiciona o meu usuário ao grupo whell
- Adiciona a minha chave ssh ao usuário criado anteriormente
- Instala alguns pacotes como   'curl', 'vim', 'git', 'ufw','fail2ban'

## 1 - Clonando o repo e entrando na pasta
$git clone git@github.com:onovaes/ansible-playbooks.git
cd ansible-playbooks

## 2 - Editar arquivo de configuração 
$vim ubuntu_initial_setup/vars/default.yml

## Executar playbook

Executaremos como root na primeira vez.

$ansible-playbook -u root ubuntu_initial_setup/playbook.yml 

