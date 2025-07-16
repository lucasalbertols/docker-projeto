# Site Apache com Docker Compose

Projeto mínimo para servir um site HTML simples usando **Apache (httpd)** em um container Docker, orquestrado via **Docker Compose**.

---

## Estrutura

```
site-apache-docker/
├── docker-compose.yml
└── site/
    └── index.html
```

---

## Como usar localmente

> Se o seu computador estiver lento e você não conseguir rodar Docker, basta enviar este repositório no GitHub conforme instruções abaixo.  
> Caso queira tentar rodar:

```bash
docker-compose up -d
```

Depois acesse: <http://localhost:8080>

---

## Passos para subir no GitHub

1. Faça login no GitHub e crie um novo repositório (por ex.: `site-apache-docker`).
2. Baixe/extraia este projeto localmente.
3. No terminal, dentro da pasta do projeto:

```bash
git init
git add .
git commit -m "Projeto Apache com Docker Compose"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/site-apache-docker.git
git push -u origin main
```

Substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub.

---

## Teste rápido sem Docker (só para ver o HTML)

Abra o arquivo `site/index.html` diretamente no navegador com duplo clique.  
Não será servido via Apache, mas você verá o conteúdo.

---

## Créditos

Projeto preparado para o Lucas por IA assistente.  
Data de geração: 2025-07-16 23:38:59
