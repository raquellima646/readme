# readme
🧪 CHIPUS - Ferramenta de Coleta e Rastreabilidade de Requisitos
Sistema web para gerenciamento automatizado de testes de semicondutores, desenvolvido para a Chipus Microeletrônica, substituindo processos manuais repetitivos por uma plataforma centralizada e eficiente.


🏢 Empresa Parceira
CHIPUS
 Empresa fabless fundada em 2008, especializada em:
ASICs Turnkey de sinal misto


Blocos IP


Design de Circuitos Integrados (IC)


📍 Sede: Florianópolis – SC
 🌍 Atuação: EUA, Europa e Ásia

Contexto do Projeto
A Chipus Microeletrônica enfrentava desafios na gestão de dados de testes de semicondutores:
Processos manuais repetitivos e propensos a erros
Dificuldade no armazenamento e organização de dados de testes
Falta de rastreabilidade nos processos de validação de ASICs
Solução: Desenvolvimento de uma plataforma web para automatizar a coleta, organização e rastreabilidade de requisitos de testes.


Funcionalidades Principais
Autenticação e Segurança
Login corporativo com e-mail e senha da empresa
Interface administrativa protegida
Gestão de Projetos
Criação e organização de projetos de testes
Vinculação com Google Sheets e Google Drive
Visualização de todos os projetos em cards organizados
Controle de Testes
Registro detalhado de cada teste (nome, índice, resultado, seed, tag)
Status visual (PASSOU/FALHOU) com identificação rápida
Histórico de atividades recentes

Relatórios e Rastreabilidade
Geração de relatórios detalhados por projeto
Informações completas de cada teste:
Rastreabilidade (TRC)
RTL (Register Transfer Level)
Versão do ambiente
Último executor
Exportação para PDF
Operações CRUD
Criar novos projetos
Visualizar detalhes completos
Atualizar informações do projeto
Excluir projetos quando necessário

Stack Tecnológica
Frontend
HTML5, CSS3, JavaScript
Design responsivo e intuitivo
Paleta de cores alinhada com identidade visual da Chipus
Ferramentas de Desenvolvimento
IDE: Visual Studio Code
Design/Prototipação: Figma/Adobe XD
Documentação: Google Docs/Sheets
Controle de Versão: Git
Integrações
Google Sheets API
Google Drive API
Google Cloud Platform

Arquitetura do Sistema

Instalação e Configuração
Pré-requisitos
Node.js (v16 ou superior)
NPM ou Yarn
Conta Google Cloud Platform (para APIs)
Acesso ao Google Workspace (para autenticação corporativa)
Passos para Configuração
1. Clonar o repositório
git clone https://github.com/seu-usuario/chipus-web-app.git
cd chipus-web-app

2. Instalar dependências

npm install
# ou
yarn install



3. Configurar variáveis de ambiente
Crie um arquivo .env na raiz:
GOOGLE_CLIENT_ID=seu_client_id_aqui
GOOGLE_API_KEY=sua_api_key_aqui
SESSION_SECRET=seu_secret_aqui
DATABASE_URL=url_do_banco
APP_ENV=development

4. Configurar Google APIs
Acessar Google Cloud Console
Criar novo projeto
Habilitar Google Sheets API e Google Drive API
Criar credenciais OAuth 2.0
5. Executar aplicação
bash
#Ambiente de desenvolvimento
npm run dev

#Build para produção
npm run build


Telas do Sistema
1. Login (/login)
Tela de autenticação corporativa
Validação de e-mail e senha
Design alinhado com branding Chipus
2. Dashboard (/dashboard)
Visão geral das atividades
Cards de projetos recentes
Feed de atividades


3. Gestão de Projetos (/projects)
Listagem de todos os projetos
Cards com informações resumidas
Botões de ação (novo, editar, excluir)
4. Detalhes do Projeto (/projects/:id)
Tabela completa de testes
Estatísticas do projeto
Links para planilhas e documentos
Botões de modificação e exclusão
5. Relatórios (/reports)
Visualização de relatórios gerados
Informações detalhadas de rastreabilidade
Botões para exportar PDF

Modelo de Dados
Projeto

{
  id: "string",
  name: "string",
  spreadsheetUrl: "string",
  driveUrl: "string",

  testCount: "number",
  createdAt: "timestamp",
  updatedAt: "timestamp"
}

Teste
{
  id: "string",
  projectId: "string",
  index: "string",       // Ex: "T.01"
  name: "string",        // Ex: "#TKILL1"
  result: "string",      // "PASSOU" ou "FALHOU"
  seed: "string",
  tag: "string",
  executor: "string",
  traceability: "string", // Ex: "TRC-GMA-001"
  rtl: "string",         // Ex: "RTL-2024-001"
  environmentVersion: "string",
  executedAt: "timestamp"
}

Equipe de Desenvolvimento
Julielen Arnoud
Milena Castro
Raquel da Silva
Kimberlin Rodrigues
Samuel Walter

Próximas Funcionalidades (Roadmap)
Integração contínua com sistemas da Chipus
Notificações em tempo real
Dashboard analítico com gráficos
API RESTful completa
App móvel complementar
Automação de testes via integração direta


Licença
Este projeto foi desenvolvido para a Chipus Microeletrônica como parte de um projeto acadêmico/parceria. O código é propriedade intelectual da equipe de desenvolvimento.



Impacto Esperado
Redução de 80% no tempo de registro de testes
Eliminação de erros manuais na transcrição
Rastreabilidade completa do ciclo de testes
Centralização de todos os dados em uma plataforma
Automação de processos repetitivos

✅ Pontos Fortes (Já incluídos):
✅ Visão geral do projeto
✅ Contexto do problema e solução
✅ Funcionalidades principais detalhadas
✅ Stack tecnológica
✅ Arquitetura do sistema
✅ Instalação e configuração passo a passo
✅ Modelo de dados
✅ Equipe de desenvolvimento
✅ Roadmap futuro
✅ Informações de contato

script para deixar pronto o servidor e criamos pasta de autenticação e projetos e seus respectivos arquivos internos;
Ajeitamos com o Marcio o servidor para fazer a simulação, script para automatizar a transferencia  dos log para o drive;
 
Deve ser criado um arquivo usuários.json e projetos.json e colocar o caminho deles no arquivo config.ini!!!

Para o admin do servidor (já estar logado no servidor):
1-	Va até onde quer salvar criar as informações de usuário;
2-	Use o comando “nano ~/Documents/Autenticacao/usuarios.json” (caminho de exemplo, usar o que quiser)
3-	Digitar usuários nesse formato:
{
"ana": "senha123",
"bruno": "palavra_secreta",
"samuel": "gama_experience"
}
Para salvar CTRL + X, pressionar “y” e ENTER.

Windows

Criação de uma chave SSH (no pc do usuário):
1-	Abra do CMD;
2-	Digite o código “ssh-keygen -t rsa -b 4096”
3-	Apertar ENTER 3 vezes para criar uma chave SSH sem password
4-	Digite o comando no CMD “type %USERPROFILE%\.ssh\id_rsa.pub | ssh -p PortaDoServidor NomeDoServidor@IPdoServidor "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 700 ~/.ssh && chmod 600 ~/.ssh/authorized_keys"”, Ele vai pedir a senha do seu servidor uma última vez para autorizar a nova chave.
A pasta deve ter permissão 700 e os id_ssh devem ter permissão 600
