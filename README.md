
<td style="width: 20%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/Logo_CEFET-MG.png" width="20%" /></td>
<p><strong><span style="color: #0000ff;"> SO Debian SBC OrangePI</span></strong></p>
<p><strong><span style="color: #0000ff;">Prof Epaminondas Lage</span></strong></p>
<a href="http://lattes.cnpq.br/7787341723868111"> Currículo Lattes LAGE, E. S.</a> 


<td style="width: 15%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/em%20constru%C3%A7%C3%A3o.jpg" width="15%" /></td>

# Índice 

* [Introdução](#Introdução)

# Introdução

# SO Debian SBC OrangePI

1) Baixar a imagem oficial no site da orangepi: http://www.orangepi.org/html/hardWare/computerAndMicrocontrollers/service-and-support/Orange-pi-One.html
- Selecionei a versão debian > server (terminal) pois é mais leve que a desktop (que possui interface gráfica)
- No meu caso baixei a versão: OrangePi_one_debian_stretch_server_linux5.3.5_v1.0.tar.gz

2) Extrair o arquivo baixado

3) Utilizar algum programa de flash de imagem. No meu caso eu utilizei o BalenaEtcher
- Selecione o arquivo.img extraido do download
- Selecione o cartão de memória que está conectado ao computador para gravar
- Clique me flash e aguarde

4) Conecte o sd card na orangepi e ligue um cabo de rede e a entrada hdmi, além de um teclado usb

5) Após ligar a orangepi, faça login com o usuário root e a senha orangepi

6) Digite ifconfig para visualizar o ip da orangepi em sua rede.

7) Apartir deste momento é possivel continuar usando o hdmi + teclado ou acessar a placa via rede usando o comando ssh root@<ip>
- após usar o comando confirme e digite a senha orangepi para efetuar a conexão

8) Após logar na orangepi, utilize os seguintes comandos:
fdisk -c /dev/mmcblk0
d
2
np
p
2
143360
62333951
n
w
reboot

10) faça login novamente via ssh ou tela

11) utilize o seguinte comando:
resize2fs /dev/mmcblk0p2

12) instale o openplc:
git clone https://github.com/thiagoralves/OpenPLC_v3.git
cd OpenPLC_v3
./install.sh linux

13) o comando acima vai demorar bastante para compilar. Aguarde finalizar e então reinicie o equipamento com o seguinte comando:
reboot

14) acesse a interface web no seguinte endereço: http://<ip>:8080
- O usuário padrão é: openplc
- A senha padrão é: openplc


# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)


