# 🚀 Projeto: Site HTML com Apache usando Docker Compose

Este projeto tem como objetivo demonstrar o uso do Docker e Docker Compose para servir um site HTML simples através do servidor Apache (httpd).

## 🧠 Motivação

Este desafio foi proposto com a finalidade de praticar os conhecimentos em containers Docker, gerenciamento de serviços com Docker Compose e publicação de aplicações básicas em ambiente isolado e versionado.

## 🛠️ Tecnologias Utilizadas

- **Docker**
- **Docker Compose**
- **Apache HTTP Server (httpd:2.4)**
- **HTML5**

## 🗂️ Estrutura do Projeto

```
site-apache-docker/
├── docker-compose.yml     # Arquivo que define e orquestra os serviços
├── .gitignore             # Ignora arquivos desnecessários no versionamento
├── README.md              # Este arquivo com instruções do projeto
└── site/
    └── index.html         # Página HTML servida pelo Apache
```

## ⚙️ Como Executar Localmente

### 1. Pré-requisitos

- Docker e Docker Compose instalados  
(https://www.docker.com/products/docker-desktop)

### 2. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/site-apache-docker.git
cd site-apache-docker
```

### 3. Rodar o container

```bash
docker-compose up -d
```

Acesse no navegador:  
👉 http://localhost:8080

Você verá a mensagem:  
**"Olá, mundo! Estou rodando no Apache via Docker Compose!"**

---

## 📦 Sobre o `docker-compose.yml`

```yaml
version: '3.8'

services:
  web:
    image: httpd:2.4
    container_name: apache-html
    ports:
      - "8080:80"
    volumes:
      - ./site:/usr/local/apache2/htdocs/
```

- Utiliza a imagem oficial do Apache
- Mapeia a porta 8080 do host para a 80 do container
- Serve o conteúdo HTML da pasta local `site/`

---

## 🧪 Teste Local (sem Docker)

Você também pode visualizar o HTML abrindo diretamente o arquivo:

```
site/index.html
```

Basta dar dois cliques nele para abrir no navegador (sem Apache, só o HTML).

---

## 📝 Conclusão

Este projeto me ajudou a entender melhor como criar ambientes isolados com Docker, como servir aplicações estáticas e como organizar arquivos em containers com Docker Compose.

> Feito com dedicação por **Lucas Alberto** 💻
