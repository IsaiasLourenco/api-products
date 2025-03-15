# API REST - Node e Express

> API REST usando Node.js e Express.js com dois endpoints de produtos

```
# Rotas
GET      /api/products
GET      /api/product/:id

```

## Uso

```
# Instalar dependências
npm install
ou
yarn install

# Rodar em desenvolvimento
npm run dev
ou
yarn run dev

# Rodar em produção
npm start
ou
yarn start
```

# 15/03/2025 - Verificado problema ao buscar produto por ID

- No arquivo server.js na linha 7, ele estava buscando
- app.get('/api/product/:id', getProduct);
- E tendo o retorno →
- Cannot GET /api/products/2, se o produto buscado era o 2
- Foi mudado para 
- app.get('/api/products/:id', getProduct);
- E agora está buscando normalmente:
- {
  "id": "2",<br>
  "name": "iPhone 11 Pro 256GB Memory",<br>
  "description": "Introducing the iPhone 11 Pro. A transformative triple-camera system that adds tons of capability without complexity. An unprecedented leap in battery life",
  "price": 599.99<br>
}
