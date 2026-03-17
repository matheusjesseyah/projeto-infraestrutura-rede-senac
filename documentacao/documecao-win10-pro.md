# Documentação de Instalação do Windows 10 Pro

## Introdução
Esta documentação fornece um guia passo a passo detalhado para a instalação do Windows 10 Pro em um computador. Este processo é parte do projeto de infraestrutura de rede do SENAC, visando demonstrar conhecimentos em configuração de sistemas operacionais.

## Requisitos do Sistema
Antes de iniciar a instalação, verifique se o hardware atende aos requisitos mínimos do Windows 10 Pro:

- **Processador:** 1 GHz ou superior (recomendado: 2 GHz ou superior)
- **Memória RAM:** 2 GB (recomendado: 4 GB ou mais)
- **Espaço em disco:** 20 GB (recomendado: 50 GB ou mais)
- **Gráficos:** DirectX 9 ou superior com driver WDDM 1.0
- **Resolução de tela:** 800x600 ou superior
- **Conexão com a internet:** Necessária para ativação e atualizações

## Preparação dos Materiais
### 1. Download da ISO do Windows 10 Pro
1. conseguimos a ISO do windows 10 Acessando o site oficial da Microsoft: [https://www.microsoft.com/pt-br/software-download/windows10](https://www.microsoft.com/pt-br/software-download/windows10) 
2. Clique em "Download da ferramenta agora" para baixar a Media Creation Tool.
3. Execute a ferramenta e selecione "Criar mídia de instalação para outro computador".
4. Escolha a edição "Windows 10 Pro" e a arquitetura (32-bit ou 64-bit, dependendo do hardware).
5. Baixe a ISO ou crie um USB bootável diretamente.

### 2. Criação de Mídia Bootável
#### Opção A: USB Bootável
1. Baixe o Rufus: [https://rufus.ie/](https://rufus.ie/)
2. Insira um USB de pelo menos 8 GB.
3. Execute o Rufus e selecione a ISO do Windows 10.
4. Clique em "Iniciar" para criar o USB bootável.

#### Opção B: DVD
1. Use um software como o Windows Disc Image Burner (integrado no Windows) ou ImgBurn.
2. Grave a ISO em um DVD virgem.

## Processo de Instalação
### 1. Configuração da BIOS/UEFI
1. Reinicie o computador e entre na BIOS (geralmente pressionando F2, F10, Del ou Esc durante o boot).
2. Desative o Secure Boot (se necessário).
3. Defina a ordem de boot para priorizar USB ou DVD.
4. Salve as alterações e saia da BIOS.

### 2. Início da Instalação
1. Insira o USB/DVD bootável e reinicie o computador.
2. O computador irá carregar o instalador do Windows.
3. Selecione o idioma, formato de hora e moeda, e layout do teclado.
4. Clique em "Instalar agora".

### 3. Chave do Produto
1. Insira a chave do produto do Windows 10 Pro (se disponível).
2. Se não tiver, clique em "Não tenho uma chave do produto" para instalar sem ativar (pode ativar posteriormente).

### 4. Seleção da Edição
1. Escolha "Windows 10 Pro".
2. Aceite os termos de licença.

### 5. Tipo de Instalação
1. Selecione "Personalizada: Instalar somente o Windows (avançado)".
2. Selecione a partição onde instalar o Windows (recomendado: formatar e criar nova partição).

### 6. Instalação Automática
1. Aguarde a instalação (pode levar 20-40 minutos).
2. O computador reiniciará automaticamente várias vezes.

## Configuração Pós-Instalação
### 1. Configuração Inicial
1. Escolha a região e layout do teclado.
2. Conecte-se à internet (Wi-Fi ou Ethernet).
3. Entre com uma conta Microsoft ou crie uma conta local.

### 2. Atualizações
1. Vá para Configurações > Atualização e Segurança > Windows Update.
2. Instale todas as atualizações disponíveis.

### 3. Drivers e Software Essencial
1. Instale drivers para placa de vídeo, áudio, etc., do site do fabricante.
2. Instale software básico: navegador, antivírus, etc.

### 4. Configurações de Rede
1. Configure IP estático ou DHCP conforme o projeto de rede.
2. Teste a conectividade com ping e outros comandos.

## Solução de Probleblemas Comuns
- **Erro de boot:** Verifique a ordem de boot na BIOS.
- **Instalação travando:** Desconecte dispositivos USB não essenciais.
- **Ativação falhando:** Verifique a chave do produto e conexão com internet.
- **Drivers ausentes:** Baixe do site do fabricante do hardware.

## Conclusão
Esta instalação configura um ambiente básico do Windows 10 Pro. Para o projeto SENAC, considere integrar com configurações de rede, como servidor DHCP e outros serviços de infraestrutura.

## Referências
- Documentação oficial da Microsoft: [https://support.microsoft.com/windows](https://support.microsoft.com/windows)
- Requisitos do sistema: [https://www.microsoft.com/windows/windows-10-specifications](https://www.microsoft.com/windows/windows-10-specifications)