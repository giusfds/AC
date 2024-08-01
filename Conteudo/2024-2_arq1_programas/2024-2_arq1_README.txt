PUC-Minas
Instituto de Ci�ncias Exatas e Informatica
Curso de Ci�ncia da Computa��o
Arquitetura de Computadores I

Pacote de programas para fundamentos de sistemas digitais

Itens

- 8085    v1.0 e v2.0
- CPUSim  v3.9.0
- Icarus  Verilog v.12 com GTKWave v3.3.100
- JFLAP   v7.1
- Logisim v2.16.1.x (ou superior, vers�o mais atualizada) 

Instala��o

O arquivo compactado dever� ser expandido em uma 
pasta  de  sua  prefer�ncia, por exemplo em  C:\.
Recomenda-se n�o  usar  pasta  cujo  nome  possua
espa�os em branco, acentos ou cedilha.

Os  atalhos  (.lnk)  dever�o  ser  verificados  e 
editados para corresponder a essa pasta.

Os arquivos terminados em  (.bat)  tamb�m dever�o 
ser editados para ajuste dos caminhos (path).

Recomenda-se  testar  previamente o funcionamento 
de todos os programas,  mesmo sem previs�es  para
usos imediatos.

Para maior  comodidade  sugere-se  acrescentar  �
vari�vel  de  ambiente  PATH  o  caminho  para as
pastas  que  contenham os  programas  execut�veis
(bin), principalmente o Icarus_Verilog (iverilog) 
e GTKWave.

Para realizar esse acr�scimo, no Windows, supondo
a pasta do compilador em C:\Icarus_Verilog_v12:

    Menu Iniciar
    |_ Configura��es
       |_ Procurar: vari�veis de ambiente 
          |_ Escolher: Vari�veis de ambiente do sistema
             |_ Apertar o bot�o: Vari�veis de ambiente
                |_ Procurar: Path
                   |_ Apertar o bot�o: Editar
                      |_ Apertar o bot�o: Novo
                      |  |_ Procurar o caminho: C:\Icarus_Verilgo_v12
                      |  |_ OK
                      |_ Apertar o bot�o: Novo
                      |  |_ Procurar o caminho: C:\Icarus_Verilgo_v12\bin
                      |  |_ OK
                      |_ Apertar o bot�o: Novo
                      |  |_ Procurar o caminho: C:\Icarus_Verilgo_v12\gtkwave\bin
                      |  |_ OK
                      |  |_ OK
                      |_ OK

    Nota:
    Em caso de d�vidas, procurar mais informa��es no link abaixo: 

    https://www.wikihow.com/Change-the-PATH-Environment-Variable-on-Windows

    Alternativa para abrir o Menu Iniciar � executar diretamente o comando:

    SystemPropertiesAdvanced.exe

    Testar a instala��o abrir uma janela de comandos (prompt):

    Menu Iniciar
    |_ Executar: cmd

    Ap�s a abertura da janela:

    C:\___ >iverilog -v

    E aguardar resposta indicando a vers�o (12.0).

Em linha de comando, ap�s definir a vari�vel PATH,
para se compilar um programa em Verilog, usar:

iverilog -o program.vvp program.v

A extens�o (.v) dever� ser associada ao arquivo fonte
e a exten�o  (.vvp)  dever� ser associada  ao arquivo 
objeto  cuja execu��o poder� ser feita como  descrito 
a seguir

vvp program.vvp

Recomenda-se  manter  as  extens�es  ".v"  e  ".vvp"
em min�sculas, independente do sistema operacional.
A extens�o ".vhdl" ser� reservada para outra linguagem.

Na pasta principal h� um programa exemplo "hello.v",
o qual poder� ser usado para testes

iverilog -o hello.vvp hello.v
vvp hello.vvp
 
Caso n�o seja encontrado o compilador, usar o comando:

compile.bat hello

No ambiente Linux ou no Windows WSL tamb�m poder� ser
usado comando:

./compile.sh hello

Nota: O script compile.sh precisar� ter permiss�es para
      execu��o. Se n�o as tiver, conced�-las com

      chmod +x compile.sh
  

Observa��es

Qualquer editor de textos poder� ser associado
para programas em Verilog. Sugere-se o uso de
editores nativos do pr�prio sistema operacional.

A maioria dos programas selecionados funcionar�o
em ambientes de quaisquer sistemas operacionais,
com Java, pelo menos, a vers�o 1.8.xx instalada.
O Icarus_Verilog e o GTKWAVE s�o dependentes 
de plataforma e requerem maior aten��o.

A vers�o sugerida para ambiente Windows j� est�
atualizada, manualmente, o que n�o ocorre na
vers�o de distribui��o dispon�vel no site.
Por iso, sugere-se o uso da primeira, tomando
as provid�ncias necess�rias para a sua 
localiza��o no sistema operacional.

Em ambientes Linux o Icarus_Verilog e o GTKWAVE
podem ser instalados via

sudo apt-get install iverilog gtkwave
ou
sudo apt     install iverilog gtkwave

embora as vers�es possam diferir entre sistemas,
outras ainda recentes, ser�o aceit�veis.

Caso n�o seja poss�vel instalar, recomendam-se
compiladores online gratuitos como

https://www.tutorialspoint.com/compile_verilog_online.php
https://www.jdoodle.com/execute-verilog-online/

https://www.edaplayground.com
// necess�rio cadastrar-se

Para os demais programas basta a simples c�pia
para a pasta /opt e configura��o de permiss�es
para execu��o.
