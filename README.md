# Agenda de Contatos

Este é um projeto de uma aplicação web de agenda de contatos desenvolvida com Node.js, Express e MongoDB. A aplicação permite aos usuários se cadastrarem, fazerem login e gerenciarem seus contatos pessoais.

## Tecnologias Utilizadas

- **Backend:** Node.js, Express
- **Frontend:** EJS (Embedded JavaScript Templates), Bootstrap 4
- **Banco de Dados:** MongoDB (com Mongoose)
- **Bundler:** Webpack
- **Transpilador:** Babel
- **Segurança:** bcryptjs (hash de senhas), csurf (proteção CSRF), helmet (headers HTTP seguros)
- **Sessões:** express-session, connect-mongo, connect-flash

## Estrutura do Projeto

```
.
├── frontend            # Código fonte frontend
│   ├── assets
│   │   └── css         # Arquivos CSS
│   └── main.js         # Ponto de entrada para Webpack
├── public              # Arquivos estáticos
│   └── assets
│       └── js          # JavaScript compilado (bundle)
├── src
│   ├── controllers     # Controladores da aplicação
│   ├── middleware      # Middlewares Express
│   ├── models          # Modelos de dados Mongoose
│   └── views           # Templates EJS
│       └── includes    # Componentes EJS reutilizáveis
├── .env                # Variáveis de ambiente (não versionado)
├── .gitignore          # Arquivos ignorados pelo Git
├── package.json        # Dependências e scripts npm
├── routes.js           # Configuração de rotas da aplicação
├── server.js           # Ponto de entrada da aplicação
└── webpack.config.js   # Configuração do Webpack
```

## Funcionalidades

- **Sistema de Autenticação**
  - Registro de usuários
  - Login de usuários
  - Validação de formulários
  - Proteção contra CSRF
  - Feedback de erros/sucesso com flash messages

- **Agenda de Contatos** (em desenvolvimento)
  - Visualização de contatos
  - (Previsto) Adição de novos contatos
  - (Previsto) Edição de contatos existentes
  - (Previsto) Exclusão de contatos

## Configuração e Instalação

### Pré-requisitos

- Node.js (versão recomendada: 14.x ou superior)
- MongoDB (local ou remoto)

### Passos para Instalação

1. Clone o repositório:
   ```
   git clone [URL_DO_REPOSITÓRIO]
   cd projetoAgenda
   ```

2. Instale as dependências:
   ```
   npm install
   ```

3. Crie um arquivo `.env` na raiz do projeto com a seguinte variável:
   ```
   CONNECTIONSTRING=sua_string_de_conexao_mongodb
   ```

4. Execute o webpack para compilar os assets do frontend:
   ```
   npm run dev
   ```

5. Inicie o servidor:
   ```
   npm start
   ```

6. Acesse a aplicação em:
   ```
   http://localhost:3000
   ```

## Scripts Disponíveis

- `npm start`: Inicia o servidor com nodemon (reinicia automaticamente quando há alterações)
- `npm run dev`: Executa o webpack no modo watch para compilação contínua dos assets frontend

## Segurança

A aplicação implementa diversas medidas de segurança:
- Senhas são hasheadas com bcryptjs
- Proteção contra CSRF com csurf
- Headers HTTP seguros com helmet
- Sessões seguras com cookies HttpOnly

## Estado Atual do Projeto

A aplicação está em desenvolvimento inicial, com o sistema de autenticação implementado e a estrutura básica para a agenda de contatos. A funcionalidade completa de gerenciamento de contatos (adicionar, editar, excluir) está prevista para implementação futura.

## Autor

[Nome do Autor]

## Licença

ISC
