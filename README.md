Projeto Impressora Elgin – Integração Java
📝 Descrição

Este projeto é um sistema de atendimento de caixa (PDV simplificado) desenvolvido em Java, que simula a comunicação com impressoras de cupom fiscal da Elgin.
O sistema permite realizar operações de impressão de texto, QR Code, código de barras, avanço e corte de papel, abertura de gaveta, sinal sonoro e impressão de XML SAT/cancelamento.

O objetivo do projeto é integrar lógica de programação (condicionais, laços de repetição e funções) com um cenário prático de automação comercial.

💻 Funcionalidades

O sistema permite ao usuário:

Configurar conexão com a impressora (USB, RS232, TCP/IP, Bluetooth).

Abrir e fechar a conexão com a impressora.

Imprimir texto no cupom fiscal com alinhamento, estilo e tamanho configuráveis.

Imprimir QR Code com dados, tamanho e nível de correção escolhidos pelo usuário.

Imprimir código de barras com dados, altura, largura e HRI configuráveis.

Avançar papel.

Realizar corte do papel.

Abrir gaveta de dinheiro (Elgin ou padrão).

Emitir sinal sonoro.

Imprimir XML SAT ou XML de cancelamento, escolhendo o arquivo via interface gráfica (JFileChooser).

📋 Menu Interativo

Ao executar o programa, o usuário verá o seguinte menu:

1  - Configurar Conexao
2  - Abrir Conexao
3  - Impressao Texto
4  - Impressao QRCode
5  - Impressao Cod Barras
6  - Impressao XML SAT
7  - Impressao XML Canc SAT
8  - Abrir Gaveta Elgin
9  - Abrir Gaveta
10 - Sinal Sonoro
0  - Fechar Conexao e Sair


O programa permanece em execução até que o usuário escolha a opção 0.

⚙️ Tecnologias e Bibliotecas

Java 17

JNA (Java Native Access) – Para integração com a DLL da impressora.

DLL oficial da impressora Elgin E1_Impressora01.dll

Swing (JFileChooser) para seleção de arquivos XML.

🛠️ Requisitos

Java 17 instalado.

Adicionar biblioteca JNA ao projeto.

Ter a DLL da impressora localizada no caminho correto:
C:\Users\gabri\OneDrive\Documentos\FACULDADE\Java-Aluno Graduacao\untitled\E1_Impressora01.dll

Impressora conectada (USB, RS232, TCP/IP ou Bluetooth) e ligada.

Para impressão de XML SAT ou cancelamento, arquivos XML devem estar disponíveis na máquina.

🚀 Como executar

Clone o projeto:

git clone https://github.com/GabrielMoreira48/ProjetoImpressoraElgin.git


Abra o projeto em uma IDE Java (IntelliJ, Eclipse ou VS Code).

Certifique-se de adicionar a DLL da impressora no caminho correto.

Execute a classe Main.java.

Siga o menu interativo para testar todas as funcionalidades.

🖼️ Exemplo de Uso

Escolha a opção 3 - Impressao Texto → digite alinhamento, estilo, tamanho e o texto.

Escolha a opção 4 - Impressao QRCode → digite os dados, tamanho e nível de correção.

Escolha a opção 6 - Impressao XML SAT → selecione o arquivo XML na janela de seleção.

📚 Funções da Biblioteca Elgin Utilizadas

AbreConexaoImpressora()

FechaConexaoImpressora()

ImpressaoTexto()

Corte()

ImpressaoQRCode()

ImpressaoCodigoBarras()

AvancaPapel()

AbreGavetaElgin()

AbreGaveta()

SinalSonoro()

ImprimeXMLSAT()

ImprimeXMLCancelamentoSAT()

✅ Observações

O sistema valida se a conexão com a impressora está aberta antes de executar qualquer operação de impressão.

XML SAT/cancelamento é selecionado via interface gráfica (JFileChooser), facilitando o uso pelo usuário.

Todas as funções são encapsuladas em métodos próprios, garantindo modularidade e organização do código.

📂 Estrutura do Projeto
ProjetoImpressoraElgin/
├─ src/
│  ├─ Main.java
├─ lib/
│  ├─ E1_Impressora01.dll
├─ README.md
