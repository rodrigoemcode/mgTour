# Projeto de Portfólio - Empresa de Turismo

Este projeto é uma aplicação web para uma pequena empresa de turismo que organiza viagens. O backend é desenvolvido em Flask, com um frontend estilizado utilizando Tailwind CSS. O sistema inclui funcionalidades como cadastro de clientes, agendamento de viagens, gestão de pacotes turísticos, e integração com sistemas de pagamento.

## Estrutura do Projeto

### Backend com Flask

#### Estrutura de Pastas:
- **app/**: Contém os pacotes da aplicação.
  - **templates/**: Armazena os templates HTML.
  - **static/**: Armazena arquivos estáticos como CSS, imagens e JavaScript.
  - **routes.py**: Define as rotas da aplicação.
  - **models.py**: Define os modelos de banco de dados.
  - **forms.py**: Gerencia os formulários (opcional, caso não use uma solução de frontend como Vue/React).
  - **services.py**: Contém a lógica de negócios.
  - **api.py**: Define as rotas da API REST.
- **migrations/**: Controle de migrações do banco de dados.
- **config.py**: Configurações da aplicação (ambiente, chave secreta, etc).
- **tests/**: Testes unitários e de integração.

### Frontend com Tailwind CSS

#### Instalação e Configuração:
- Use um gerenciador de pacotes como npm/yarn para instalar Tailwind CSS.
- Crie um arquivo de configuração `tailwind.config.js` para personalizar o design.
- Organize os componentes de UI de maneira modular (ex.: navegação, formulários, cartões de pacotes de viagem).

### API REST

#### Estrutura das Rotas RESTful:
- Utilize Blueprints para modularizar diferentes funcionalidades (ex.: rotas de clientes, viagens, pagamentos).
- Use uma biblioteca como Flask-RESTful ou Flask-Swagger para organizar e documentar as APIs.

### Banco de Dados

#### Configuração e Modelagem:
- Escolha um banco de dados adequado (ex.: SQLite para desenvolvimento, PostgreSQL para produção).
- Defina os modelos de dados no `models.py` para as seguintes entidades:
  - Clientes
  - Viagens
  - Pacotes de viagem
  - Pagamentos

### Sistema de Agendamento

#### Funcionalidades:
- Desenvolva um sistema para gerenciar as viagens disponíveis (datas, pacotes, disponibilidade).
- Defina rotas e lógica de reserva.
- Garanta que o calendário e a disponibilidade estejam sincronizados com o banco de dados.

### Formas de Pagamento

#### Integração:
- Integre uma API de pagamento (ex.: Stripe, PayPal) para processar transações.
- Defina modelos para armazenar informações de transações no banco de dados.

### Outras Funcionalidades

- Área de login e cadastro de clientes.
- Dashboard para o cliente gerenciar suas reservas.
- Sistema de feedback/review das viagens.

## Tecnologias e Dependências

### Backend

- **Flask**: Framework principal.
- **flask-sqlalchemy**: ORM para interações com o banco de dados.
- **flask-migrate**: Controle de migrações de banco de dados.
- **flask-wtf**: Suporte a formulários (opcional).
- **flask-restful**: Organização das APIs REST.
- **flask-login**: Gerenciamento de autenticação.

### Frontend

- **Tailwind CSS**: Framework de CSS utilitário.
- **Alpine.js** (opcional): Para interatividade leve.

### Banco de Dados

- **SQLite** (para desenvolvimento) ou **PostgreSQL** (para produção).
- **psycopg2**: Driver PostgreSQL para Python.

### Testes

- **pytest**: Framework de testes.
- **pytest-flask**: Extensão para testes em Flask.

## Outras Ferramentas

- **Gerenciador de pacotes**: pip ou poetry.
- **gunicorn** ou **uwsgi**: Para deployment em produção.
- **Docker**: Para containerização do projeto (opcional).

### Extras

- **Documentação da API**: Use o Swagger ou Postman para documentar as APIs REST.
- **Deployment**: Prepare um arquivo `Dockerfile` e um `docker-compose.yml` para o projeto.
