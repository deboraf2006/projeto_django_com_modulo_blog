# Blog em Django

Blog feito com Django 5, com posts, comentários, tags, compartilhamento por e-mail, sitemap e PostgreSQL.

## Requisitos

- Python 3.13
- Docker Desktop (para o PostgreSQL)

## Como rodar

1. Baixe o projeto e entre na pasta:

   ```
   git clone URL-DO-REPOSITORIO
   cd NOME-DA-PASTA
   ```

2. Crie e ative o ambiente virtual:

   ```
   python -m venv my_env
   my_env\Scripts\activate
   ```

3. Instale as dependências:

   ```
   pip install -r requirements.txt
   ```

4. Copie o arquivo de exemplo para `.env` e preencha os valores:

   ```
   copy .env.example .env
   ```

5. Suba o banco de dados (com o Docker aberto):

   ```
   docker compose up -d
   ```

6. Crie as tabelas e um usuário administrador:

   ```
   python manage.py migrate
   python manage.py createsuperuser
   ```

7. Rode o servidor:

   ```
   python manage.py runserver
   ```

Acesse `http://127.0.0.1:8000/blog/`. O painel de administração fica em `/admin/`.

## E-mail

Para o compartilhamento por e-mail funcionar, é preciso uma senha de app do Gmail no `.env`.