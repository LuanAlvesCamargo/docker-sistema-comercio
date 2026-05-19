# docker-sistema-comercio

# Projeto Final — Plataforma E-commerce de Imóveis

## Informações Gerais

Projeto desenvolvido em grupo com dois alunos.

### Integrantes

- Luan
- Mathes

---

# Entregas Obrigatórias

## Entregáveis do Projeto

- Projeto funcional utilizando Docker Compose
- Documentação do projeto (.doc)
- Slides de apresentação (.ppt)
- Resumo para Jornada Científica
  - Tema: Containers vs Máquinas Virtuais
- Artigo para Revista
  - Tema: Kubernetes vs. Red Hat OpenShift: Uma Análise Comparativa para Administradores de Sistemas e DevOps

---

# Organização das Responsabilidades

## Luan

Responsável por:

- Documentação do projeto (.doc)
- Slides de apresentação (.ppt)
- Resumo para Jornada Científica
  - Containers vs Máquinas Virtuais
- Artigo para Revista
  - Kubernetes vs. Red Hat OpenShift: Uma Análise Comparativa para Administradores de Sistemas e DevOps

---

## Mathes

Responsável por:

- Desenvolvimento do projeto
- Estrutura Docker
- Backend
- Banco de dados
- Configuração da aplicação

---

# Projeto Funcional

## Descrição

Desenvolvimento de um MVP de uma Plataforma E-commerce de Imóveis.

---

# Requisitos Obrigatórios

## Estrutura mínima obrigatória

- Dockerfile
- docker-compose.yml
- Frontend com no mínimo 5 telas
- Variáveis de ambiente
- Persistência de dados
- Redes Docker

---

# Tecnologias Utilizadas

## Backend

- PHP
- Laravel

## Bancos de Dados

### MySQL

Banco de produtos

### PostgreSQL

Banco principal da aplicação

### MariaDB

Banco de logs e cache

---

# Arquitetura

## Arquitetura da Aplicação

- Monolito MVC

---

# Estrutura do Projeto

```txt
meu-projeto-faculdade/
├── .docker/                         # Configurações customizadas dos containers
│   ├── nginx/
│   │   └── default.conf             # Configuração do Frontend (Servidor Web)
│   └── php/
│       └── Dockerfile               # Configuração do Backend (PHP-FPM + Extensões)
├── app/                             # Core do Laravel (MVC)
│   ├── Http/
│   │   ├── Controllers/             # C do MVC
│   │   └── Middleware/
│   └── Models/                      # M do MVC (Organizados por Banco de Dados)
│       ├── Application/             # Models do PostgreSQL (Usuários, Pedidos...)
│       ├── Log/                     # Models do MariaDB (Logs, Auditoria)
│       └── Product/                 # Models do MySQL (Produtos, Estoque)
├── config/
│   └── database.php                 # Configuração de conexão dos 3 bancos
├── database/
│   ├── factories/
│   ├── migrations/                  # Migrações dos bancos de dados
│   └── seeders/
├── public/                          # Ponto de entrada do Nginx (index.php, CSS, JS)
├── resources/                       # V do MVC
│   └── views/                       # Telas em Blade (Frontend do Monolito)
├── routes/
│   └── web.php                      # Rotas da aplicação
├── .env                             # Variáveis de ambiente
├── .env.example
├── .gitignore
├── docker-compose.yml               # Orquestrador dos containers
└── README.md
```
