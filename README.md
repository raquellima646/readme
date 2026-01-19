# readme
CHIPUS — Ferramenta de Coleta e Rastreabilidade de Requisitos

Sistema web para gerenciamento automatizado de testes de semicondutores, desenvolvido para a Chipus Microeletrônica, com o objetivo de substituir processos manuais repetitivos por uma plataforma centralizada, segura e eficiente, garantindo rastreabilidade completa dos testes de validação de ASICs.

🏢 Empresa Parceira — Chipus Microeletrônica

A Chipus Microeletrônica é uma empresa fabless fundada em 2008, especializada em:

ASICs turnkey de sinal misto

Desenvolvimento de blocos IP

Design de Circuitos Integrados (IC)

📍 Sede: Florianópolis – SC
🌍 Atuação: Estados Unidos, Europa e Ásia
🔗 Site: https://chipus.com

📌 Contexto do Projeto

A Chipus enfrentava diversos desafios na gestão de dados de testes de semicondutores, entre eles:

Processos manuais repetitivos e suscetíveis a erros

Dificuldade no armazenamento e organização dos dados de testes

Ausência de rastreabilidade no processo de validação de ASICs

💡 Solução Proposta

Desenvolvimento de uma plataforma web para automatizar a coleta, organização e rastreabilidade dos requisitos de testes, centralizando informações e otimizando o fluxo de validação.

⚙️ Funcionalidades Principais
🔐 Autenticação e Segurança

Login corporativo com e-mail e senha

Interface administrativa protegida

📁 Gestão de Projetos

Criação e organização de projetos de testes

Vinculação com Google Sheets e Google Drive

Visualização de projetos em cards organizados

🧪 Controle de Testes

Registro detalhado de cada teste:

Nome

Índice

Resultado

Seed

Tag

Status visual (PASSOU / FALHOU)

Histórico de atividades recentes

📊 Relatórios e Rastreabilidade

Geração de relatórios detalhados por projeto

Informações completas de cada teste:

Rastreabilidade (TRC)

RTL (Register Transfer Level)

Versão do ambiente

Último executor

Exportação de relatórios em PDF

🔄 Operações CRUD

Criar projetos

Visualizar detalhes

Atualizar informações

Excluir projetos

🛠️ Stack Tecnológica
Frontend

HTML5

CSS3

JavaScript

Design responsivo e intuitivo

Paleta de cores alinhada à identidade visual da Chipus

Ferramentas de Desenvolvimento

IDE: Visual Studio Code

Design/Prototipação: Figma / Adobe XD

Documentação: Google Docs / Google Sheets

Controle de Versão: Git

Integrações

Google Sheets API

Google Drive API

Google Cloud Platform

🏗️ Arquitetura do Sistema

O sistema é baseado em uma arquitetura web modular, integrando autenticação, gestão de projetos, controle de testes e geração de relatórios, com suporte a APIs externas do Google para armazenamento e sincronização de dados.

🚀 Instalação e Configuração
Pré-requisitos

Node.js (v16 ou superior)

NPM ou Yarn

Conta no Google Cloud Platform

Acesso ao Google Workspace (autenticação corporativa)

Passos para Configuração
1️⃣ Clonar o repositório
git clone https://github.com/seu-usuario/chipus-web-app.git
cd chipus-web-app

2️⃣ Instalar dependências
npm install
# ou
yarn install

3️⃣ Configurar variáveis de ambiente

Crie um arquivo .env na raiz do projeto:

GOOGLE_CLIENT_ID=seu_client_id_aqui
GOOGLE_API_KEY=sua_api_key_aqui
SESSION_SECRET=seu_secret_aqui
DATABASE_URL=url_do_banco
APP_ENV=development

4️⃣ Configurar Google APIs

Acessar o Google Cloud Console

Criar um novo projeto

Habilitar Google Sheets API e Google Drive API

Criar credenciais OAuth 2.0

5️⃣ Executar a aplicação
# Ambiente de desenvolvimento
npm run dev

# Build para produção
npm run build

🖥️ Telas do Sistema
🔑 Login (/login)

Autenticação corporativa

Validação de credenciais

Interface alinhada ao branding da Chipus

📊 Dashboard (/dashboard)

Visão geral das atividades

Cards de projetos recentes

Feed de atividades

📁 Gestão de Projetos (/projects)

Listagem completa de projetos

Cards com informações resumidas

Ações: criar, editar e excluir

📄 Detalhes do Projeto (/projects/:id)

Tabela completa de testes

Estatísticas do projeto

Links para planilhas e documentos

Opções de modificação e exclusão

📑 Relatórios (/reports)

Visualização de relatórios gerados

Informações detalhadas de rastreabilidade

Exportação em PDF

🗂️ Modelo de Dados
Projeto
{
  "id": "string",
  "name": "string",
  "spreadsheetUrl": "string",
  "driveUrl": "string",
  "testCount": "number",
  "createdAt": "timestamp",
  "updatedAt": "timestamp"
}

Teste
{
  "id": "string",
  "projectId": "string",
  "index": "string",
  "name": "string",
  "result": "PASSOU | FALHOU",
  "seed": "string",
  "tag": "string",
  "executor": "string",
  "traceability": "string",
  "rtl": "string",
  "environmentVersion": "string",
  "executedAt": "timestamp"
}

👥 Equipe de Desenvolvimento

Julielen Arnoud

Milena Castro

Raquel da Silva

Kimberlin Rodrigues

Samuel Walter

🔮 Roadmap (Próximas Funcionalidades)

Integração contínua com sistemas internos da Chipus

Notificações em tempo real

Dashboard analítico com gráficos

API RESTful completa

Aplicativo móvel complementar

Automação de testes via integração direta

📈 Impacto Esperado

Redução de 80% no tempo de registro de testes

Eliminação de erros manuais de transcrição

Rastreabilidade completa do ciclo de testes

Centralização total dos dados

Automação de processos repetitivos

📄 Licença

Este projeto foi desenvolvido para a Chipus Microeletrônica como parte de um projeto acadêmico/parceria.
O código é propriedade intelectual da equipe de desenvolvimento e da Chipus Microeletrônica.

📬 Contato

Parceiro Industrial: Chipus Microeletrônica
📍 Florianópolis – SC, Brasil
🌐 https://chipus.com

Para questões técnicas, utilize o repositório do projeto.

📄Textos em inglês:
Readme
🧪 CHIPUS — Test Requirement Collection and Traceability Tool

Web-based system for automated semiconductor test management, developed for Chipus Microeletrônica, aiming to replace repetitive manual processes with a centralized, secure, and efficient platform, ensuring full traceability of ASIC validation tests.

🏢 Partner Company — Chipus Microeletrônica

Chipus Microeletrônica is a fabless company founded in 2008, specialized in:

Mixed-signal turnkey ASICs

IP block development

Integrated Circuit (IC) design

📍 Headquarters: Florianópolis, SC — Brazil
🌍 Operations: United States, Europe, and Asia
🔗 Website: https://chipus.com

📌 Project Context

Chipus faced several challenges in managing semiconductor test data, including:

Repetitive and error-prone manual processes

Difficulty in storing and organizing test data

Lack of traceability in the ASIC validation process

💡 Proposed Solution

Development of a web platform to automate the collection, organization, and traceability of test requirements, centralizing information and optimizing the validation workflow.

⚙️ Main Features
🔐 Authentication & Security

Corporate login using email and password

Protected administrative interface

📁 Project Management

Creation and organization of test projects

Integration with Google Sheets and Google Drive

Project visualization using organized cards

🧪 Test Control

Detailed test records including:

Name

Index

Result

Seed

Tag

Visual status (PASS / FAIL)

Recent activity history

📊 Reports & Traceability

Generation of detailed reports per project

Complete test information:

Traceability (TRC)

RTL (Register Transfer Level)

Environment version

Last executor

PDF export

🔄 CRUD Operations

Create projects

View project details

Update project information

Delete projects

🛠️ Technology Stack
Frontend

HTML5

CSS3

JavaScript

Responsive and intuitive design

Color palette aligned with Chipus branding

Development Tools

IDE: Visual Studio Code

Design / Prototyping: Figma / Adobe XD

Documentation: Google Docs / Google Sheets

Version Control: Git

Integrations

Google Sheets API

Google Drive API

Google Cloud Platform

🏗️ System Architecture

The system is based on a modular web architecture, integrating authentication, project management, test control, and report generation modules, with support for Google external APIs for data storage and synchronization.

🚀 Installation & Setup
Prerequisites

Node.js (v16 or higher)

NPM or Yarn

Google Cloud Platform account

Google Workspace access (corporate authentication)

Setup Steps
1️⃣ Clone the repository
git clone https://github.com/your-username/chipus-web-app.git
cd chipus-web-app

2️⃣ Install dependencies
npm install
# or
yarn install

3️⃣ Configure environment variables

Create a .env file in the project root:

GOOGLE_CLIENT_ID=your_client_id_here
GOOGLE_API_KEY=your_api_key_here
SESSION_SECRET=your_secret_here
DATABASE_URL=database_url_here
APP_ENV=development

4️⃣ Configure Google APIs

Access Google Cloud Console

Create a new project

Enable Google Sheets API and Google Drive API

Create OAuth 2.0 credentials

5️⃣ Run the application
# Development environment
npm run dev

# Production build
npm run build

🖥️ System Screens
🔑 Login (/login)

Corporate authentication

Credential validation

Interface aligned with Chipus branding

📊 Dashboard (/dashboard)

Activity overview

Recent project cards

Activity feed

📁 Project Management (/projects)

Complete project listing

Summary cards

Actions: create, edit, delete

📄 Project Details (/projects/:id)

Complete test table

Project statistics

Links to spreadsheets and documents

Edit and delete options

📑 Reports (/reports)

Generated report visualization

Detailed traceability information

PDF export

🗂️ Data Model
Project
{
  "id": "string",
  "name": "string",
  "spreadsheetUrl": "string",
  "driveUrl": "string",
  "testCount": "number",
  "createdAt": "timestamp",
  "updatedAt": "timestamp"
}

Test
{
  "id": "string",
  "projectId": "string",
  "index": "string",
  "name": "string",
  "result": "PASS | FAIL",
  "seed": "string",
  "tag": "string",
  "executor": "string",
  "traceability": "string",
  "rtl": "string",
  "environmentVersion": "string",
  "executedAt": "timestamp"
}

👥 Development Team

Julielen Arnoud

Milena Castro

Raquel da Silva

Kimberlin Rodrigues

Samuel Walter

🔮 Roadmap (Future Features)

Continuous integration with Chipus internal systems

Real-time notifications

Analytical dashboard with charts

Full RESTful API

Companion mobile application

Automated test execution integration

📈 Expected Impact

80% reduction in test registration time

Elimination of manual transcription errors

Full test lifecycle traceability

Centralized data management

Automation of repetitive processes

📄 License

This project was developed for Chipus Microeletrônica as part of an academic/industrial partnership.
The source code is the intellectual property of the development team and Chipus Microeletrônica.

📬 Contact

Industrial Partner: Chipus Microeletrônica
📍 Florianópolis, SC — Brazil
🌐 https://chipus.com

For technical questions, please use the project repository.

