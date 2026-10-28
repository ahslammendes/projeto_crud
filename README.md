# Sistema de Autenticação e CRUD de Usuários

Este projeto é uma aplicação em Python desenvolvida para demonstrar o gerenciamento completo de usuários (CRUD - *Create, Read, Update, Delete*) e um fluxo de autenticação web utilizando **SQLAlchemy**, **Werkzeug** e **Streamlit**.

---

## 🚀 Funcionalidades

- **CRUD de Usuários**:
  - Cadastro de novos usuários com nome, email e nível de acesso (`acesso_gestor`).
  - Consulta de todos os usuários ou busca específica por `id`.
  - Atualização cadastral de dados e senha.
  - Exclusão de usuários.
- **Segurança e Hashing de Senhas**:
  - Armazenamento seguro de senhas no banco de dados através de hash criptográfico (`generate_password_hash` e `check_password_hash` do Werkzeug).
- **Interface Web com Streamlit**:
  - Tela de login interativa.
  - Validação de credenciais em tempo real com controle de estado de sessão (`st.session_state`).
- **Banco de Dados SQLite**:
  - Criação automática da tabela no banco SQLite local através do SQLAlchemy ORM.

---

## 🛠️ Tecnologias Utilizadas

- [Python 3.10+](https://www.python.org/)
- [SQLAlchemy](https://www.sqlalchemy.org/) - Mapeamento Objeto-Relacional (ORM)
- [Streamlit](https://streamlit.io/) - Framework para interface web interativa
- [Werkzeug](https://werkzeug.palletsprojects.com/) - Criptografia e validação de senhas
- [SQLite](https://www.sqlite.org/) - Banco de dados embutido

---

## 📁 Estrutura do Projeto

```text
CRUD/
├── CRUD.py              # Modelos ORM e funções de manipulação do banco (CRUD)
├── tela.py              # Interface gráfica web (Streamlit) para autenticação
├── requirements.txt     # Dependências do projeto
├── .gitignore           # Arquivos e pastas ignorados pelo Git
└── README.md            # Documentação do projeto
```

---

## ⚙️ Como Executar o Projeto

### 1. Pré-requisitos

Certifique-se de ter o Python instalado na sua máquina.

### 2. Clonar o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd CRUD
```

### 3. Criar e ativar um ambiente virtual (recomendado)

- **Windows:**
  ```bash
  python -m venv .venv
  .venv\Scripts\activate
  ```

- **Linux / macOS:**
  ```bash
  python3 -m venv .venv
  source .venv/bin/activate
  ```

### 4. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 5. Executar a aplicação

Para iniciar a interface web com o Streamlit:

```bash
streamlit run tela.py
```

O aplicativo será aberto automaticamente no seu navegador padrão (geralmente em `http://localhost:8501`).

---

## 📝 Observações

- Na primeira execução de `CRUD.py` ou de `tela.py`, o arquivo de banco de dados `bd_usuarios.sqlite` será criado automaticamente caso ainda não exista.

