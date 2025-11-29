# Servidor de Monitoramento de Tempo

Objetivo: Instalação e configuração do ambiente Node.js, Express e ferramentas de desenvolvimento. Introdução ao roteamento (rotas e métodos HTTP) para Back-End.

## Descrição

Este projeto implementa um servidor web básico utilizando Node.js e Express, criando uma aplicação que responde a requisições HTTP.

## Requisitos

- Node.js (versão recomendada: 14.x ou superior)
- npm (gerenciador de pacotes do Node.js)

## Instalação

### Passo 1: Clonar o Repositório

```bash
git clone https://github.com/Vilander/001--servidor-de-monitoramento-de-tempo.git
cd 001--servidor-de-monitoramento-de-tempo
```

### Passo 2: Instalar Dependências

```bash
npm install
```

Este comando irá instalar as dependências listadas no `package.json`, incluindo:

- **Express** (^5.1.0) - Framework web para Node.js

## Execução

### Iniciar o Servidor

```bash
node index.js
```

O servidor será iniciado e ficará escutando na **porta 3000**.

### Acessar o Serviço

Abra seu navegador e acesse:

```
http://localhost:3000/
```

Você deverá ver a mensagem: **"Serviço Operacional"**

## Estrutura do Projeto

```
001--servidor-de-monitoramento-de-tempo/
├── index.js          # Arquivo principal da aplicação
├── package.json      # Dependências e configurações do projeto
├── README.md         # Este arquivo
└── LICENSE           # Licença MIT
```

## Código Principal

O servidor foi implementado com a seguinte estrutura:

```javascript
const express = require("express");
const app = express();

app.get("/", function (req, res) {
  res.send("Serviço Operacional");
});

app.listen(3000);
```

### Explicação:

1. **Importar Express**: `const express = require("express");` - Carrega o framework Express
2. **Criar Aplicação**: `const app = express();` - Cria uma instância da aplicação
3. **Definir Rota**: `app.get("/", ...)` - Define uma rota GET para o caminho raiz (`/`)
4. **Enviar Resposta**: `res.send("Serviço Operacional");` - Retorna uma mensagem ao cliente
5. **Iniciar Servidor**: `app.listen(3000);` - Coloca o servidor escutando na porta 3000

## Scripts Disponíveis

No arquivo `package.json`, você pode adicionar scripts para facilitar a execução:

### Desenvolvimento Contínuo (com Nodemon)

Para reiniciar automaticamente o servidor quando há alterações:

```bash
npm install --save-dev nodemon
```

Depois, adicione ao `package.json`:

```json
"scripts": {
  "start": "node index.js",
  "dev": "nodemon index.js",
  "test": "echo \"Error: no test specified\" && exit 1"
}
```

Então execute:

```bash
npm run dev
```

## Informações do Projeto

- **Nome**: 001--servidor-de-monitoramento-de-tempo
- **Versão**: 1.0.0
- **Tipo**: CommonJS
- **Autor**: Vilander Costa
- **Licença**: MIT
- **Repositório**: https://github.com/Vilander/001--servidor-de-monitoramento-de-tempo

## Próximos Passos

- [ ] Adicionar mais rotas (GET, POST, PUT, DELETE)
- [ ] Implementar middleware
- [ ] Adicionar tratamento de erros
- [ ] Integrar banco de dados
- [ ] Adicionar testes unitários
- [ ] Configurar variáveis de ambiente

## Licença

Este projeto é licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.
