<div align="center">

# 🎓 Conecta Fatec

### Rede social acadêmica para estudantes, professores e comunidade universitária.

O **Conecta Fatec** é um projeto acadêmico desenvolvido para criar um ambiente digital de conexão, interação e colaboração dentro do contexto universitário. A plataforma busca aproximar estudantes, professores e membros da comunidade acadêmica por meio de publicações, perfis, amizades e comunidades temáticas.

[![Frontend](https://img.shields.io/badge/Frontend-HTML%20%7C%20CSS%20%7C%20JavaScript-blue)](#-tecnologias)
[![Backend](https://img.shields.io/badge/Backend-Python%20%7C%20Django%20REST-green)](#-tecnologias)
[![Status](https://img.shields.io/badge/Status-Em%20desenvolvimento-yellow)](#-status-do-projeto)
[![Projeto](https://img.shields.io/badge/Projeto-Acad%C3%AAmico-purple)](#-sobre-o-projeto)

</div>

---

## 📌 Sobre o projeto

O **Conecta Fatec** foi criado com a proposta de funcionar como uma rede social voltada ao ambiente acadêmico, oferecendo um espaço para troca de conhecimento, divulgação de ideias, interação entre alunos e fortalecimento da comunidade universitária.

A aplicação é composta por duas partes principais:

- **Frontend:** responsável pela interface visual e pela experiência do usuário.
- **Backend:** responsável pela API, autenticação, regras de negócio e gerenciamento dos dados.

Essa divisão permite uma estrutura mais organizada, facilitando a manutenção, a evolução do projeto e o trabalho em equipe.

---

## 🚀 Funcionalidades principais

- Cadastro e login de usuários.
- Autenticação com token JWT.
- Perfil de usuário com foto, curso, nickname e biografia.
- Feed de publicações.
- Criação, edição e exclusão de posts.
- Curtidas em posts e comentários.
- Comentários em publicações.
- Respostas em comentários.
- Sistema de amizades entre usuários.
- Solicitações de amizade enviadas e recebidas.
- Criação e participação em comunidades.
- Publicações dentro de comunidades.
- Páginas institucionais, como Sobre, Termos de Uso e Política de Cookies.
- Interface responsiva para desktop e dispositivos móveis.

---

## 🧱 Organização dos repositórios

| Repositório | Descrição | Tecnologias |
|---|---|---|
| `conecta-frontend` | Interface web da rede social acadêmica. | HTML, CSS, JavaScript, Bootstrap/Tailwind via CDN |
| `conecta-backend` | API REST responsável pelos dados, autenticação e regras do sistema. | Python, Django, Django REST Framework, JWT |

---

## 🖥️ Frontend

O frontend representa a camada visual do projeto. Ele foi desenvolvido com tecnologias web tradicionais e organiza as principais telas da aplicação, como login, cadastro, feed, perfil, amizades, comunidades, notificações e configurações.

### Principais características

- Layout responsivo.
- Componentes visuais reutilizáveis.
- Páginas separadas por área da aplicação.
- Integração com a API do backend.
- Uso de JavaScript para interações dinâmicas.
- Estrutura visual voltada para uma experiência moderna e acadêmica.

---

## ⚙️ Backend

O backend é responsável por fornecer os recursos necessários para o funcionamento da rede social. Ele foi desenvolvido com **Python**, **Django** e **Django REST Framework**, seguindo o modelo de uma API REST.

### Principais responsabilidades

- Gerenciamento de usuários.
- Autenticação com JWT.
- Controle de perfis.
- Gerenciamento de posts.
- Sistema de comentários e respostas.
- Sistema de curtidas.
- Sistema de amizades.
- Gerenciamento de comunidades.
- Comunicação com banco de dados.
- Controle das regras de negócio da aplicação.

---

## 🧰 Tecnologias

### Frontend

- HTML5
- CSS3
- JavaScript
- Bootstrap/Tailwind via CDN

### Backend

- Python
- Django
- Django REST Framework
- Simple JWT
- SQLite
- PostgreSQL
- Cloudinary
- CORS Headers
- Gunicorn
- Whitenoise

---

## 🔐 Autenticação

A autenticação do sistema é baseada em **JWT**, permitindo que usuários acessem recursos protegidos da plataforma de forma segura após o login.

---

## 🌐 Deploy

- **Frontend:** `https://conecta-fatec.github.io/conecta-frontend/`
- **API:** `https://conecta-fatec-api.onrender.com`

---

## 📌 Status do projeto

🚧 Projeto em desenvolvimento.

O sistema ainda está em evolução e pode receber melhorias futuras, como aprimoramentos de interface, ajustes de responsividade, novas interações sociais, sistema de notificações mais completo, melhorias de acessibilidade e testes automatizados.

---

## 🎯 Objetivo acadêmico

O projeto tem como objetivo aplicar conhecimentos de desenvolvimento web, integração entre frontend e backend, consumo de APIs, autenticação, modelagem de dados e organização de um sistema completo em equipe.

---

<div align="center">

**Conecta Fatec — conectando ideias, pessoas e conhecimento.**

</div>
