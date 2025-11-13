# Projeto Impressora Elgin – Integração Java

Este projeto demonstra como realizar a comunicação com impressoras Elgin utilizando Java e a biblioteca JNA (Java Native Access).  
O objetivo é exemplificar funções como abertura de conexão, impressão de texto, QRCode, sinal sonoro, abertura de gaveta e finalização da conexão.

---

## 📌 Tecnologias utilizadas
- Java 17+
- JNA 5.15.0
- Biblioteca Elgin DLL (E1\_Impressora.dll)
- IntelliJ IDEA Community
- Git + GitHub

---

## 🚀 Funcionalidades implementadas
### ✔ Abertura de Conexão USB  
Permite iniciar comunicação com a impressora via porta USB.

### ✔ Impressão de Texto  
Exemplo simples utilizando funções nativas disponibilizadas pela DLL.

### ✔ Impressão de QR Code  
Geração e envio de QR Code diretamente para a impressora.

### ✔ Sinal Sonoro  
Função para emitir bipes através da impressora.

### ✔ Abertura de Gaveta  
Comando que envia pulso elétrico para abrir gaveta de dinheiro compatível.

### ✔ Encerramento de Conexão  
Finaliza a comunicação com a impressora de forma segura.

---

## 🧩 Exemplo de Função: Sinal Sonoro

```java
public static void SinalSonoro() {
    if (conexaoAberta) {
        int resultado = ImpressoraDLL.INSTANCE.SinalSonoro(4, 5, 5);

        if (resultado == 0) {
            System.out.println("Sinal emitido com sucesso");
        } else {
            System.out.println("Erro ao emitir o sinal! Erro: " + resultado);
        }

    } else {
        System.out.println("Conexão não iniciada!");
        return;
    }
}
```

---

## 📁 Estrutura do Projeto

```
ProjetoImpressoraElgin/
 ├─ libs/
 │   └─ jna-5.15.0.jar
 ├─ src/
 │   └─ main/java/
 │       └─ Impressora/
 │            ├─ Main.java
 │            └─ ImpressoraDLL.java
 ├─ README.md
 └─ build.gradle
```

---

## 🔧 Como executar
1. Instale o Java 17+
2. Adicione o JNA ao projeto
3. Coloque a DLL na pasta correta
4. Execute pelo IntelliJ (botão run)
5. Certifique-se de que a impressora está conectada ao USB

---

## 👤 Autores

**Carlos Gabriel Moreira**  
GitHub: github.com/GabrielMoreira48  

**Gabriel **

GitHub

**Guilherme Nogueira**	
GitHub

**Kauan Medeiros**
GitHub:  github.com/Hyazaka

**Murilo Rodrigues**
GitHub: github.com/batatalouca821k-blip

Projeto desenvolvido para fins acadêmicos e prática de integração com dispositivos externos.


