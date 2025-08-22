# Projeto Imobiliária (Versão Terminal com SQLite)

## 📄 Descrição

Este projeto é um **sistema de gerenciamento imobiliário** desenvolvido em **Java** para execução no **terminal**. Ele permite gerenciar **clientes**, **imóveis** e **contratos**, armazenando os dados em um banco **SQLite**.

---

## ✨ Funcionalidades

* Cadastro de clientes
* Cadastro de imóveis
* Criação e gerenciamento de contratos
* Persistência de dados utilizando banco **SQLite**
* Estrutura baseada em **DAO** (Data Access Object)

---

## 🛠 Como foi desenvolvido

* **Linguagem:** Java 17+
* **Gerenciador de dependências:** Maven
* **Banco de dados:** SQLite (arquivo `.db`)
* **Execução:** Terminal utilizando `mvn exec:java`

---

## 🔧 Pré-requisitos

Para rodar este projeto, você precisa instalar e configurar:

1. **Java JDK 17 ou superior**

2. **Maven**

   * Baixar o Apache Maven: [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi)
   * Extrair e colocar a pasta (por exemplo, `apache-maven-3.9.11`) em **C:\maven**
   * Configurar as **variáveis de ambiente**:

     * `MAVEN_HOME = C:\maven\apache-maven-3.9.11`
     * Adicionar `C:\maven\apache-maven-3.9.11\bin` na variável **PATH**

3. **SQLite**

   * Baixar o SQLite: [https://www.sqlite.org/download.html](https://www.sqlite.org/download.html)
   * Colocar o executável (`sqlite3.exe`) em `C:\sqlite`

4. **Banco de dados**

   * O arquivo `imobiliaria.db` deve estar na pasta do projeto.

---

## 🔍 Estrutura do projeto

```
imobiliaria_terminal_sqlite_v2/
├── pom.xml                # Configuração do Maven
├── imobiliaria.db         # Banco de dados SQLite
├── src/
│   └── main/java/br/com/imobiliaria/
│       ├── Main.java      # Classe principal
│       ├── dao/           # Classes DAO
│       ├── model/         # Modelos de dados
│       └── util/DbUtil.java # Conexão com SQLite
└── resources/schema.sql    # Script do banco
```

---

## 🔢 Como configurar o ambiente

1. Coloque a pasta **do Maven** em `C:\maven`

<img width="1919" height="1052" alt="Maven" src="https://github.com/user-attachments/assets/dd7d85d0-1daf-4b79-8196-639bf19762be" />


2. Configure as variáveis de ambiente:

   * `MAVEN_HOME`
   * Adicione `bin` do Maven ao **PATH**

<img width="1561" height="585" alt="Variáveis de Ambiente - Maven" src="https://github.com/user-attachments/assets/a23546c9-5d79-4169-9301-7d797d12dc88" />

3. Coloque o executável do **SQLite** em `C:\sqlite`

<img width="1919" height="1050" alt="SQLite" src="https://github.com/user-attachments/assets/45fc6202-3d6b-46bc-8434-3c1974ee415a" />


4. Certifique-se de que o arquivo `imobiliaria.db` está na pasta do projeto.


---

## 🛠 Como rodar no terminal

### 1. Navegue até a pasta do projeto:

```bash
cd C:\CAMINHO\PARA\imobiliaria_terminal_sqlite_v2
```

*(Substitua pelo caminho da sua máquina)*

### 2. Execute o projeto com Maven:

```bash
C:\maven\apache-maven-3.9.11\bin\mvn.cmd -q -Dexec.mainClass=br.com.imobiliaria.Main org.codehaus.mojo:exec-maven-plugin:3.5.0:java
```

### 3. Para acessar o banco de dados via SQLite:

```bash
C:\sqlite\sqlite3.exe imobiliaria.db
```

---

## 🔹 Observações importantes

* **Sempre substitua os caminhos de exemplo** pelos caminhos reais da sua máquina.
* Verifique se as variáveis de ambiente estão configuradas corretamente para o Maven funcionar.
* Caso ocorra erro de conexão, cheque se o arquivo `imobiliaria.db` está no local correto.

---

## 📊 Exemplo de execução completa

```bash
cd C:\Users\SeuUsuario\Desktop\imobiliaria_terminal_sqlite_v2
C:\maven\apache-maven-3.9.11\bin\mvn.cmd -q -Dexec.mainClass=br.com.imobiliaria.Main org.codehaus.mojo:exec-maven-plugin:3.5.0:java
```

Para abrir o banco:

```bash
C:\sqlite\sqlite3.exe imobiliaria.db![Uploading Variáveis de Ambiente - Maven.png…]()

```

---

## 🛠 Comandos úteis do SQLite

Dentro do SQLite, você pode usar:

```sql
.tables         -- Lista as tabelas
.schema         -- Mostra a estrutura
SELECT * FROM Cliente;   -- Exemplo de consulta
```

---

## 📝 Autores

João Vitor Rosera,
Marcelo Vinicius Leicht,
Vinicius Werner

Projeto desenvolvido como exemplo de **sistema imobiliário** em **Java + SQLite** com execução em **terminal**.
