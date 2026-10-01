<div align="center">

# 🛒 Sistema de Gerenciamento de Loja

**Aplicação Java com banco de dados PostgreSQL, usando o padrão DAO e operações CRUD**

![Java](https://img.shields.io/badge/Java-100%25-orange?logo=openjdk&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-JDBC-336791?logo=postgresql&logoColor=white)
![Padrão](https://img.shields.io/badge/Padrão-DAO-blue)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

</div>

---

## 📖 Sobre o projeto

Projeto desenvolvido como trabalho de avaliação da disciplina de **Banco de Dados 2** do curso de **Engenharia de Software** do **UNIFSA (Centro Universitário Santo Agostinho)**.

O sistema simula a gestão de uma loja, permitindo cadastrar e manipular **clientes**, **produtos** e **pedidos**, com a comunicação com o banco feita via **JDBC** e organizada através do **padrão DAO (Data Access Object)**.

---

## ✨ Funcionalidades

- 👤 **Clientes**: cadastro, consulta, atualização e remoção
- 📦 **Produtos**: operações CRUD completas
- 🧾 **Pedidos**: registro e gerenciamento de pedidos
- 🔌 **Conexão centralizada** com o PostgreSQL em uma única classe

---

## 🗂️ Estrutura do repositório

```
Trabalho-codigos-avalia-aoBD2/
├── Conexao.java       # Conexão com o PostgreSQL (JDBC)
├── ClienteDAO.java    # Acesso a dados de clientes
├── ProdutoDAO.java    # Acesso a dados de produtos
├── PedidoDAO.java     # Acesso a dados de pedidos
├── Main.java          # Classe principal (execução)
└── README.md
```

### 🧠 Como funciona o padrão DAO (explicação simples)

Em vez de espalhar comandos SQL por todo o código, cada tabela tem uma classe responsável por conversar com ela:

```
Main  ──►  ClienteDAO / ProdutoDAO / PedidoDAO  ──►  Conexao  ──►  PostgreSQL
```

Assim o código fica mais organizado, fácil de manter e de reaproveitar.

---

## 🚀 Como executar

### Pré-requisitos

- [JDK 17+](https://adoptium.net/)
- [PostgreSQL](https://www.postgresql.org/download/) instalado e em execução
- [Driver JDBC do PostgreSQL](https://jdbc.postgresql.org/download/) (arquivo `.jar`)

### Passo a passo

```bash
# 1. Clone o repositório
git clone https://github.com/guilhermeestrela10/Trabalho-codigos-avalia-aoBD2.git

# 2. Entre na pasta
cd Trabalho-codigos-avalia-aoBD2
```

**3. Crie o banco de dados** no PostgreSQL e as tabelas usadas pelos DAOs (clientes, produtos e pedidos).

**4. Ajuste a conexão** na classe `Conexao.java` com a URL, o usuário e a senha do seu banco:

```java
// Exemplo
String url = "jdbc:postgresql://localhost:5432/nome_do_banco";
String usuario = "postgres";
String senha = "sua_senha";
```

**5. Compile e execute** (substitua o caminho do `.jar` pelo do seu driver):

```bash
# Windows
javac -cp ".;postgresql.jar" *.java
java -cp ".;postgresql.jar" Main

# Linux / macOS
javac -cp ".:postgresql.jar" *.java
java -cp ".:postgresql.jar" Main
```

> 💡 No **VS Code** ou **IntelliJ**, basta adicionar o `.jar` do driver às bibliotecas do projeto e rodar a classe `Main`.

---

## 🛠️ Tecnologias

- ☕ **Java**
- 🐘 **PostgreSQL**
- 🔗 **JDBC**
- 🐙 **Git & GitHub**

---

## 👨‍💻 Autor

**Guilherme Henrique Macedo Estrela** (Gui)
Estudante de Engenharia de Software — UNIFSA

[![GitHub](https://img.shields.io/badge/GitHub-guilhermeestrela10-181717?logo=github)](https://github.com/guilhermeestrela10)

---

<div align="center">

Feito com ☕ e PostgreSQL

</div>
