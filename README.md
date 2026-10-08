# Containeriza-o-com-Docker-e-Esteira-de-CI-com-GitHub-Actions

Trabalho prático individual para containerização com Docker, orquestração com Docker Compose, automação de CI com GitHub Actions e qualidade de código com ESLint, Prettier e Husky da matéria de ntrodução à Integração e Entrega Contínua (IEC).
## 📌 Sobre a Aplicação

A **DieselParts API** é uma API RESTful desenvolvida para o cadastro e gerenciamento de **veículos movidos a diesel**. A aplicação permite cadastrar, consultar, atualizar e excluir veículos, armazenando informações como placa, marca, modelo, ano, capacidade de carga, quilometragem, tipo de combustível e status.

## 📁 Estrutura do Repositório

O projeto está organizado em uma estrutura que separa a aplicação backend dos arquivos de configuração e infraestrutura:

```text
.
├── .github/              # Configurações do GitHub Actions
├── .husky/               # Git Hooks para validações locais
├── backend/              # Código-fonte da API
│   ├── dist/             # Arquivos compilados
│   ├── src/              # Código-fonte principal
│   ├── .env              # Variáveis de ambiente
│   ├── .env.example      # Exemplo das variáveis de ambiente
│   ├── package.json      # Dependências e scripts do backend
│   ├── README.md         # Documentação específica do backend
│   ├── requests.http    # Requisições para testes da API
│   └── tsconfig.json     # Configuração do TypeScript
├── .dockerignore         # Arquivos ignorados pelo Docker
├── .env.example          # Exemplo das variáveis de ambiente
├── .gitignore            # Arquivos ignorados pelo Git
├── .prettierignore       # Arquivos ignorados pelo Prettier
├── .prettierrc.json      # Configuração do Prettier
├── docker-compose.yml     # Orquestração dos containers
├── Dockerfile             # Configuração da imagem Docker
├── package.json            # Dependências e scripts do projeto
├── pnpm-lock.yaml          # Controle das versões das dependências
└── README.md               # Documentação principal do projeto






## Instalação e execução

### Pré-requisitos

Antes de iniciar o projeto, certifique-se de ter instalado:

* [Node.js](https://nodejs.org/) — versão 20 ou superior
* npm — instalado junto com o Node.js
* [PostgreSQL](https://www.postgresql.org/) — banco de dados utilizado pela aplicação
* Git — para clonar o repositório

### 1. Clonar o repositório

```bash
git clone URL_DO_REPOSITORIO
cd NOME_DO_PROJETO
```

### 2. Instalar as dependências

Execute o comando abaixo na pasta do projeto:

```bash
npm install
```

### 3. Configurar as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto e configure as informações necessárias para conexão com o banco de dados:

```env
PORT=3000
DATABASE_URL=postgresql://usuario:senha@localhost:5432/nome_do_banco
```

Substitua `usuario`, `senha` e `nome_do_banco` pelos dados do seu PostgreSQL.

### 4. Criar o banco de dados

No PostgreSQL, crie um banco de dados para a aplicação.

Depois, execute as configurações/migrações do projeto, caso estejam disponíveis:

```bash
npx sequelize-cli db:migrate
```

### 5. Executar o projeto

Para iniciar a aplicação em modo de desenvolvimento:

```bash
npm run dev
```

Após iniciar, a API estará disponível em:

```text
http://localhost:3000
```

### 6. Testar a aplicação

Para executar os testes:

```bash
npm test
```

Para verificar a qualidade do código:

```bash
npm run lint
```

### 7. Executar em modo de produção

Para gerar a versão de produção:

```bash
npm run build
```

Depois, execute:

```bash
npm start
```

### Resumo dos comandos

```bash
# Instalar dependências
npm install

# Executar em desenvolvimento
npm run dev

# Executar testes
npm test

# Verificar código
npm run lint

# Gerar build
npm run build

# Executar produção
npm start
```

