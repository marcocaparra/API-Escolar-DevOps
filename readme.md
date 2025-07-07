# Imersão DevOps - Alura Google Cloud

Este projeto é uma API desenvolvida com FastAPI para gerenciar alunos, cursos e matrículas em uma instituição de ensino.

## 📸 Preview da Minha Aplicação no Projeto

Durante a imersão, eu (Marco Caparra) fiz dois posts dentro do meu LinkedIn, mostrando imagens e contando cada detalhe sobre
o projeto, aulas e experiências. E abaixo desta mensagem estão os links pros dois posts!

> 👀 **Post 1**: [Clique aqui para acessar o post da aula 1 e 2](https://www.linkedin.com/posts/marco-caparra-b20b5a333_devops-docker-github-activity-7346330101766098944-jGux?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFP_ksgBN6ccTjfnbT5DTD4IIRQLNzkZoUoD)  
> 📺 **Post 2**: [Clique aqui para acessar o post da aula 3 (última)](https://www.linkedin.com/posts/marco-caparra-b20b5a333_ontem-dando-continuidade-%C3%A0-minha-jornada-activity-7346881469547499520-xff0?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFP_ksgBN6ccTjfnbT5DTD4IIRQLNzkZoUo)  

## Pré-requisitos

- [Python 3.10 ou superior instalado](https://www.python.org/downloads/)
- [Git](https://git-scm.com/downloads)
- [Docker](https://www.docker.com/get-started/)

## Passos para subir o projeto

1. **Faça o download do repositório:**
   [Clique aqui para realizar o download](https://github.com/guilhermeonrails/imersao-devops/archive/refs/heads/main.zip)

2. **Crie um ambiente virtual:**
   ```sh
   python3 -m venv ./venv
   ```

3. **Ative o ambiente virtual:**
   - No Linux/Mac:
     ```sh
     source venv/bin/activate
     ```
   - No Windows, abra um terminal no modo administrador e execute o comando:
   ```sh
   Set-ExecutionPolicy RemoteSigned
   ```

     ```sh
     venv\Scripts\activate
     ```

4. **Instale as dependências:**
   ```sh
   pip install -r requirements.txt
   ```

5. **Execute a aplicação:**
   ```sh
   uvicorn app:app --reload
   ```

6. **Acesse a documentação interativa:**

   Abra o navegador e acesse:  
   [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

   Aqui você pode testar todos os endpoints da API de forma interativa.

## Passos para subir o projeto com Docker

Com o Docker e o Docker Compose instalados, você pode subir a aplicação com um único comando.

1. **Construa a imagem e suba o contêiner:**
   ```sh
   docker-compose up --build
   ```

2. **Acesse a documentação interativa:**
   Abra o navegador e acesse:  
   [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## Estrutura do Projeto

- `app.py`: Arquivo principal da aplicação FastAPI.
- `models.py`: Modelos do banco de dados (SQLAlchemy).
- `schemas.py`: Schemas de validação (Pydantic).
- `database.py`: Configuração do banco de dados SQLite.
- `routers/`: Diretório com os arquivos de rotas (alunos, cursos, matrículas).
- `requirements.txt`: Lista de dependências do projeto.
- `Dockerfile`: Define a imagem Docker para a aplicação.
- `docker-compose.yml`: Orquestra o contêiner da aplicação.

---

- O banco de dados SQLite será criado automaticamente como `escola.db` na primeira execução.
- Para reiniciar o banco, basta apagar o arquivo `escola.db` (isso apagará todos os dados).

---
