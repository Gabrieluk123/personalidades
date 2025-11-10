# Projeto de API REST em Go (API de Exemplo)

> API RESTful de exemplo construída com Go para [Descreva o objetivo principal aqui, ex: "gerenciar um CRUD de usuários", "demonstrar o uso de X", etc.].

---

##  Pré-requisitos

Antes de começar, certifique-se de que você tem o seguinte software instalado em sua máquina:

* **[Go](https://go.dev/dl/)**: Versão 1.18 ou superior.
* **[Docker](https://www.docker.com/get-started)**: Para rodar o banco de dados.
* **[Docker Compose](https://docs.docker.com/compose/install/)**
* **(Opcional) [Postman](https://www.postman.com/) ou [Insomnia](https://insomnia.rest/)**: Para testar os endpoints da API.

---

##  Rodando o Projeto Localmente

Siga os passos abaixo para executar a aplicação em seu ambiente local.

### 1. Clone o Repositório

```bash
# Clone este repositório
git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)

# Acesse a pasta do projeto
cd seu-repositorio
```

### 2. Inicialize o Banco de Dados

Este projeto usa Docker Compose para gerenciar o banco de dados (ex: PostgreSQL, MySQL).

```bash
# Inicia o(s) container(s) em segundo plano (detached mode)
docker-compose up -d
```

### 3. Instale as Dependências (Opcional)

Se você acabou de clonar o projeto, baixe as dependências do Go:

```bash
go mod tidy
```

### 4. Execute a Aplicação

Finalmente, rode o servidor da API:

```bash
go run main.go
```

Pronto! A API deve estar rodando em `http://localhost:8080` (ou na porta que você configurou).

---

##  Endpoints da API

Aqui estão os principais endpoints disponíveis e como usá-los.

### Recurso X (ex: /usuarios)

* **`GET /usuarios`**: Lista todos os usuários.
* **`GET /usuarios/{id}`**: Busca um usuário específico pelo ID.
* **`POST /usuarios`**: Cria um novo usuário.
    * **Corpo (Body) esperado (JSON):**
        ```json
        {
          "nome": "Seu Nome",
          "email": "email@exemplo.com"
        }
        ```

* **`PUT /usuarios/{id}`**: Atualiza um usuário existente.
* **`DELETE /usuarios/{id}`**: Remove um usuário.

---

##  Tecnologias Utilizadas

* **Linguagem:** [Go](https://go.dev/)
* **Banco de Dados:** [PostgreSQL](https://www.postgresql.org/) (via Docker)
* **Roteador:** [gorilla/mux](https://github.com/gorilla/mux) ````
