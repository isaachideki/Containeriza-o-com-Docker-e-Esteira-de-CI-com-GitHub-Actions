# Containeriza-o-com-Docker-e-Esteira-de-CI-com-GitHub-Actions

Trabalho prático individual para containerização com Docker, orquestração com Docker Compose, automação de CI com GitHub Actions e qualidade de código com ESLint, Prettier e Husky da matéria de ntrodução à Integração e Entrega Contínua (IEC).
## 📌 Sobre a Aplicação

A **Diesel Vehicles API** é uma API RESTful desenvolvida para o cadastro e gerenciamento de **veículos movidos a diesel**. A aplicação permite cadastrar, consultar, atualizar e excluir veículos, armazenando informações como placa, marca, modelo, ano, capacidade de carga, quilometragem, tipo de combustível e status.

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
