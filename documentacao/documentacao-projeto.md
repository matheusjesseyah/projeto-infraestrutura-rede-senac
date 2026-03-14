DOCUMENTAÇÃO DO PROJETO DE REDE
1. Objetivo do Projeto
Implementar uma infraestrutura de rede funcional utilizando máquinas físicas com diferentes sistemas operacionais para simular um ambiente corporativo (empresa de e-commerce). O projeto inclui 2 clientes Windows Pro, servidor de domínio (Windows Server 12 R2), servidor web Linux com WordPress e um servidor Linux atuando como firewall.
 
2. Estrutura da Rede
Equipamentos utilizados:
- Notebook 1: Windows 10 Pro (Cliente)
- Notebook 2: Windows 10 Pro (Cliente)
- Servidor 1: Windows Server 2012 R2 (Active Directory / DNS / DHCP)
- Servidor 2: Debian Linux (Servidor Web + WordPress)
- Servidor 3: Debian Linux (Firewall)
- Switch de rede para interligação dos equipamentos.


3. Planejamento de Endereçamento IP

Rede: 192.168.30.0/24

Firewall: 192.168.30.1
Windows Server: 192.168.30.10
Servidor Web Debian: 192.168.30.20
Notebook 1: 192.168.30.100
Notebook 2: 192.168.30.101

Máscara: 255.255.255.0
Gateway: 192.168.30.1
DNS: 192.168.30.10


4. Instalação do Firewall Debian
Durante a instalação do Debian selecionamos apenas:
- Servidor SSH
- Utilitários de sistema padrão

Após a instalação executamos:
apt update
apt upgrade -y

Instalação do UFW (Firewall)
apt install ufw
ufw allow ssh
ufw allow 80
ufw allow 443
ufw enable

Ativar roteamento no Linux
Editar o arquivo:
/etc/sysctl.conf

Descomentar a linha:
net.ipv4.ip_forward=1

Aplicar configuração:
sysctl -p


5. Instalação do Servidor Web Debian
Instalamos pacotes necessários:
apt update
apt install apache2 mariadb-server php php-mysql wget unzip
Download e instalação do WordPress
wget https://wordpress.org/latest.zip
unzip latest.zip
mv wordpress /var/www/html/
chown -R www-data:www-data /var/www/html/wordpress
Acesso via navegador:
http://192.168.30.20/wordpress


6. Instalação do Windows Server 2012 R2
Após instalar o sistema, adicionar funções e recursos:
- Active Directory Domain Services
- DNS Server
- DHCP Server

Criação do Domínio
Domínio utilizado:
ecommerce.noite

Configuração do DHCP
Escopo de rede:
Rede: 192.168.30.0
Range: 192.168.30.100 - 192.168.30.200
Gateway: 192.168.30.1
DNS: 192.168.30.10


7. Configuração dos Clientes Windows 10
Configurar os computadores para receber IP automaticamente via DHCP.

Entrar no domínio:
Painel de Controle > Sistema > Alterar configurações > Alterar
Selecionar domínio e digitar:
ecommerce.noite


8. Testes Realizados
Teste de conectividade:
ping 192.168.0.10
ping 192.168.0.20

Teste de acesso ao servidor web:
Abrir navegador e acessar:
http://192.168.0.20

Teste de autenticação:
Login no domínio utilizando usuário criado no Active Directory.


9. Conclusão
O projeto demonstrou a integração entre sistemas Windows e Linux dentro de uma rede corporativa. Foram implementados serviços essenciais como autenticação centralizada, servidor web e firewall para controle de segurança da rede.
