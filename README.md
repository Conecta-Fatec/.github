<div align="center">

# 🎓 Conecta Fatec

### Rede social acadêmica para conectar estudantes, professores e a comunidade universitária.

O **Conecta Fatec** é um projeto acadêmico desenvolvido com o objetivo de criar um ambiente digital colaborativo para alunos da Fatec. A plataforma permite que usuários criem perfis, publiquem conteúdos, interajam com postagens, participem de comunidades e formem conexões acadêmicas.

[![Frontend](https://img.shields.io/badge/Frontend-HTML%20%7C%20CSS%20%7C%20JavaScript-blue)](#-frontend)
[![Backend](https://img.shields.io/badge/Backend-Python%20%7C%20Django%20REST-green)](#-backend)
[![Status](https://img.shields.io/badge/Status-Em%20desenvolvimento-yellow)](#-status-do-projeto)
[![Projeto Acadêmico](https://img.shields.io/badge/Projeto-Acad%C3%AAmico-purple)](#-sobre-o-projeto)

</div>

---

## 📌 Sobre o projeto

O **Conecta Fatec** foi pensado como uma rede social voltada ao ambiente universitário, com foco em integração, colaboração e troca de conhecimento entre estudantes.

A aplicação é dividida em duas partes principais:

- **Frontend:** interface web responsável pela experiência do usuário.
- **Backend:** API REST responsável pela autenticação, regras de negócio e persistência dos dados.

A arquitetura desacoplada facilita a manutenção do projeto, a divisão de tarefas entre os integrantes do grupo e a evolução futura da aplicação.

---

## 🚀 Funcionalidades principais

- Cadastro e login de usuários.
- Autenticação com token JWT.
- Perfil do aluno com foto, curso, nickname e biografia.
- Feed de publicações.
- Criação, edição e exclusão de posts.
- Curtidas em posts e comentários.
- Comentários e respostas em comentários.
- Sistema de amizades.
- Envio, aceite, rejeição e cancelamento de solicitações de amizade.
- Criação e participação em comunidades.
- Publicações dentro de comunidades.
- Páginas institucionais, como Sobre, Termos de Uso e Política de Cookies.
- Interface responsiva para desktop e dispositivos móveis.

---

## 🧱 Estrutura da organização

| Repositório | Descrição | Tecnologias |
|---|---|---|
| `conecta-frontend` | Interface web da rede social acadêmica. | HTML, CSS, JavaScript, Bootstrap/Tailwind via CDN |
| `conecta-backend` | API REST responsável pelos dados, autenticação e regras do sistema. | Python, Django, Django REST Framework, JWT |

---

## 🎨 Frontend

O frontend foi construído com tecnologias web tradicionais, mantendo uma estrutura simples e fácil de manter.

### Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Bootstrap/Tailwind via CDN

### Principais páginas

- Login e cadastro
- Feed
- Perfil do usuário
- Perfil público de outros usuários
- Comunidades
- Página de comunidade
- Amizades
- Notificações
- Configurações
- Sobre
- Termos de uso
- Política de cookies

### Organização básica

```bash
conecta-frontend/
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── img/
│   └── js/
│       ├── main.js
│       ├── feed.js
│       ├── profile.js
│       ├── friends.js
│       ├── communities.js
│       └── post-ui.js
├── pages/
│   ├── feed.html
│   ├── profile.html
│   ├── friends.html
│   ├── communities.html
│   └── settings.html
└── index.html
```

### Como rodar o frontend localmente

Você pode abrir o projeto usando a extensão **Live Server** no Visual Studio Code ou rodar um servidor local simples:

```bash
cd conecta-frontend
python -m http.server 5500
```

Depois, acesse:

```bash
http://localhost:5500
```

Caso queira testar com o backend local, altere a variável `API_BASE_URL` no arquivo:

```bash
assets/js/main.js
```

Exemplo:

```js
const API_BASE_URL = 'http://127.0.0.1:8000';
```

---

## ⚙️ Backend

O backend foi desenvolvido com **Python**, **Django** e **Django REST Framework**, seguindo uma estrutura de API desacoplada para comunicação com o frontend.

### Tecnologias utilizadas

- Python
- Django
- Django REST Framework
- Simple JWT
- SQLite para desenvolvimento local
- PostgreSQL para ambiente em nuvem
- Cloudinary para armazenamento de imagens
- CORS Headers
- Gunicorn
- Whitenoise

### Organização básica

```bash
conecta-backend/
├── conecta_fatec/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── users/
│   ├── models.py
│   ├── serializers.py
│   ├── api_views.py
│   └── urls.py
├── posts/
│   ├── models.py
│   ├── serializers.py
│   ├── api_views.py
│   └── urls.py
├── media/
├── requirements.txt
└── manage.py
```

### Principais recursos da API

#### Usuários

- Registro de usuários.
- Login com email ou nickname.
- Perfil do usuário logado.
- Atualização de perfil.
- Perfil público por nickname.
- Sistema de amizades.

#### Posts e comentários

- Feed global.
- Criação, edição e exclusão de publicações.
- Curtidas em posts.
- Comentários em posts.
- Respostas em comentários.
- Curtidas em comentários.

#### Comunidades

- Listagem de comunidades.
- Criação de comunidades.
- Entrada e saída de comunidades.
- Posts dentro de comunidades.
- Edição e exclusão de comunidades.

### Como rodar o backend localmente

```bash
cd conecta-backend
python -m venv venv
```

Ative o ambiente virtual:

```bash
# Windows
venv\Scripts\activate

# Linux/macOS
source venv/bin/activate
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Aplique as migrações:

```bash
python manage.py migrate
```

Crie um superusuário, se necessário:

```bash
python manage.py createsuperuser
```

Inicie o servidor:

```bash
python manage.py runserver
```

A API ficará disponível em:

```bash
http://127.0.0.1:8000
```

---

## 🔐 Autenticação

A API utiliza autenticação baseada em **JWT**.

Rotas principais:

```bash
POST /api/token/
POST /api/token/refresh/
```

O frontend envia o token no cabeçalho das requisições protegidas:

```bash
Authorization: Bearer <token>
```

---

## 🔗 Principais rotas da API

### Usuários

```bash
POST   /api/users/register/
GET    /api/users/me/
PUT    /api/users/me/update/
PATCH  /api/users/me/update/
GET    /api/users/profile/<nickname>/
GET    /api/users/friends/
GET    /api/users/friend-requests/received/
GET    /api/users/friend-requests/sent/
POST   /api/users/friend-request/<nickname>/send/
POST   /api/users/friend-request/<nickname>/cancel/
POST   /api/users/friend-request/<nickname>/accept/
POST   /api/users/friend-request/<nickname>/reject/
POST   /api/users/friend/<nickname>/remove/
```

### Posts, comentários e comunidades

```bash
GET    /api/posts/feed/
POST   /api/posts/feed/create/
PUT    /api/posts/post/<post_id>/update/
PATCH  /api/posts/post/<post_id>/update/
DELETE /api/posts/post/<post_id>/delete/
POST   /api/posts/post/<post_id>/like/
POST   /api/posts/post/<post_id>/comment/

GET    /api/posts/communities/
POST   /api/posts/communities/create/
GET    /api/posts/communities/<slug>/
POST   /api/posts/communities/<slug>/post/create/
POST   /api/posts/communities/<slug>/join/
POST   /api/posts/communities/<slug>/leave/
PUT    /api/posts/communities/<slug>/update/
PATCH  /api/posts/communities/<slug>/update/
DELETE /api/posts/communities/<slug>/delete/

POST   /api/posts/comment/<comment_id>/reply/
PUT    /api/posts/comment/<comment_id>/update/
PATCH  /api/posts/comment/<comment_id>/update/
DELETE /api/posts/comment/<comment_id>/delete/
POST   /api/posts/comment/<comment_id>/like/
```

---

## 🌐 Deploy

- **Frontend:** `https://conecta-fatec.github.io/conecta-frontend/`
- **API:** `https://conecta-fatec-api.onrender.com`

---

## 🛠️ Como contribuir

Este projeto é acadêmico e desenvolvido em grupo. Para contribuir:

1. Faça um fork ou clone do repositório.
2. Crie uma branch para sua alteração.

```bash
git checkout -b feature/nome-da-funcionalidade
```

3. Faça as alterações necessárias.
4. Salve um commit com uma mensagem clara.

```bash
git add .
git commit -m "feat: add new feature"
```

5. Envie a branch para o GitHub.

```bash
git push origin feature/nome-da-funcionalidade
```

6. Abra um Pull Request para revisão.

---

## 📋 Padrão de commits sugerido

```bash
feat: nova funcionalidade
fix: correção de bug
docs: alteração na documentação
style: ajuste visual ou formatação
refactor: melhoria interna sem mudar comportamento
chore: configuração ou manutenção do projeto
```

Exemplos:

```bash
feat: add community post creation
fix: adjust friend request button layout
docs: update project setup instructions
style: improve responsive navigation design
```

---

## 📌 Status do projeto

🚧 Projeto em desenvolvimento.

Melhorias futuras podem incluir:

- Sistema de notificações totalmente funcional.
- Melhorias na responsividade mobile.
- Ajustes de acessibilidade.
- Validações mais completas no frontend.
- Testes automatizados no backend.
- Melhor organização das variáveis de ambiente.
- Deploy final com configurações de produção.

---

## 👥 Equipe

Projeto desenvolvido por estudantes da Fatec como parte de uma atividade acadêmica em grupo.

---

## ⚠️ Observações importantes

Antes de publicar o backend em produção, é recomendado revisar as configurações sensíveis do Django, como `SECRET_KEY`, `DEBUG`, `ALLOWED_HOSTS`, CORS e variáveis de ambiente.

---

<div align="center">

**Conecta Fatec — conectando ideias, pessoas e conhecimento.**

</div>
