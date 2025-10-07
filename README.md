<img width="1024" height="1024" alt="ChatGPT Image 7 de out  de 2025, 16_29_49" src="https://github.com/user-attachments/assets/80f05fb9-a03f-4a22-9340-0bcc11849f90" />


# 💊 Fast Farma

Sistema backend de gerenciamento de farmácia desenvolvido com NestJS, permitindo o controle completo de produtos e categorias de medicamentos.

## 📋 Sobre o Projeto

O Fast Farma é uma API RESTful construída para otimizar as operações diárias de uma farmácia, oferecendo funcionalidades de gerenciamento de produtos farmacêuticos organizados por categorias, facilitando o controle de estoque e a conformidade regulatória.

## 🚀 Tecnologias Utilizadas

- **NestJS** - Framework Node.js progressivo
- **TypeScript** - Superset JavaScript com tipagem estática
- **TypeORM** - ORM para manipulação do banco de dados
- **MySQL/PostgreSQL** - Sistema de gerenciamento de banco de dados
- **Class Validator** - Validação de dados
- **Class Transformer** - Transformação de objetos

## 📦 Funcionalidades

### Categorias
- ✅ Criar nova categoria
- ✅ Listar todas as categorias
- ✅ Buscar categoria por ID
- ✅ Atualizar categoria
- ✅ Deletar categoria
- ✅ Buscar categorias por descrição

### Produtos
- ✅ Criar novo produto
- ✅ Listar todos os produtos
- ✅ Buscar produto por ID
- ✅ Atualizar produto
- ✅ Deletar produto
- ✅ Buscar produtos por nome
- 🔗 Relacionamento com categorias

## 🏗️ Estrutura do Projeto

```
fast-farma/
├── src/
│   ├── categoria/
│   │   ├── entities/
│   │   │   └── categoria.entity.ts
│   │   ├── controllers/
│   │   │   └── categoria.controller.ts
│   │   ├── services/
│   │   │   └── categoria.service.ts
│   │   └── categoria.module.ts
│   ├── produto/
│   │   ├── entities/
│   │   │   └── produto.entity.ts
│   │   ├── controllers/
│   │   │   └── produto.controller.ts
│   │   ├── services/
│   │   │   └── produto.service.ts
│   │   └── produto.module.ts
│   ├── app.module.ts
│   └── main.ts
├── package.json
└── README.md
```

## 🔧 Instalação e Configuração

### Pré-requisitos
- Node.js (versão 16 ou superior)
- npm ou yarn
- MySQL ou PostgreSQL

### Passo a passo

1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/fast-farma.git
cd fast-farma
```

2. Instale as dependências
```bash
npm install
```

3. Configure as variáveis de ambiente
```bash
# Crie um arquivo .env na raiz do projeto
DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=sua_senha
DB_DATABASE=db_fastfarma
```

4. Execute as migrations (se aplicável)
```bash
npm run migration:run
```

5. Inicie a aplicação
```bash
# Modo desenvolvimento
npm run start:dev

# Modo produção
npm run start:prod
```

A aplicação estará disponível em `http://localhost:3000`

## 📡 Endpoints da API

### Categorias

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET | `/categorias` | Lista todas as categorias |
| GET | `/categorias/:id` | Busca categoria por ID |
| GET | `/categorias/descricao/:descricao` | Busca categorias por descrição |
| POST | `/categorias` | Cria nova categoria |
| PUT | `/categorias/:id` | Atualiza categoria |
| DELETE | `/categorias/:id` | Deleta categoria |

### Produtos

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET | `/produtos` | Lista todos os produtos |
| GET | `/produtos/:id` | Busca produto por ID |
| GET | `/produtos/nome/:nome` | Busca produtos por nome |
| POST | `/produtos` | Cria novo produto |
| PUT | `/produtos/:id` | Atualiza produto |
| DELETE | `/produtos/:id` | Deleta produto |

## 📝 Exemplos de Requisições

### Criar Categoria
```json
POST /categorias
{
  "tipo": "Medicamentos",
  "descricao": "Medicamentos de uso contínuo"
}
```

### Criar Produto
```json
POST /produtos
{
  "nome": "Dipirona 500mg",
  "laboratorio": "EMS",
  "preco": 12.50,
  "quantidade": 100,
  "categoria": {
    "id": 1
  }
}
```

## 🌿 Branches do Projeto

- `main` - Branch principal com código estável
- `Configurando-o-Projeto` - Configuração inicial do projeto e banco de dados
- `CRUD-Categoria` - Implementação do CRUD de categorias
- `CRUD-Produto` - Implementação do CRUD de produtos com relacionamento

## ✅ Testes

```bash
# Testes unitários
npm run test

# Testes e2e
npm run test:e2e

# Cobertura de testes
npm run test:cov
```

## 👨‍💻 Desenvolvedor

Desenvolvido como atividade prática do bootcamp Generation Brasil.

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais.

---

⭐ Desenvolvido com NestJS e TypeScript
