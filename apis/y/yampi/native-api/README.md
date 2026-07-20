# Yampi: Native API Reference

A consolidated summary of Yampi's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.yampi.com.br/api-reference/introduction
- **API base URL:** `https://api.dooki.com.br/v2`

## Authentication

### Yampi API Credentials

Direct Yampi API credentials using Alias, User Token, and User Secret Key.

### Credentials

- **Alias:** `alias` · required · The Yampi store alias used in store-scoped API paths.
- **User Token:** `userToken` · required · The User Token from Yampi Perfil > Credenciais de API.
- **User Secret Key:** `userSecretKey` · required · The User Secret Key from Yampi Perfil > Credenciais de API.

Send these headers with each API request:

```http
User-Token: <userToken>
User-Secret-Key: <userSecretKey>
```

[Official authentication documentation](https://docs.yampi.com.br/api-reference/auth/auth-user-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `scroll_id`. The total page count is read from `meta.pagination.total_pages`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 10; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | `POST /auth/me` | [docs](https://docs.yampi.com.br/api-reference/auth/auth-user-token) |
| [Get Brand](actions/get-brand.md) | `GET /:merchantAlias/catalog/brands/:id` | [docs](https://docs.yampi.com.br/api-reference/catalogo/marcas/visualizar-marca) |
| [Get Category](actions/get-category.md) | `GET /:merchantAlias/catalog/categories/:id` | [docs](https://docs.yampi.com.br/api-reference/catalogo/categorias/visualizar-categoria) |
| [Get Customer](actions/get-customer.md) | `GET /:merchantAlias/customers/:id` | [docs](https://docs.yampi.com.br/api-reference/clientes/introduction) |
| [Get Customer Address](actions/get-customer-address.md) | `GET /:merchantAlias/customers/:customerId/addresses/:id` | [docs](https://docs.yampi.com.br/api-reference/clientes/enderecos/visualizar-endereco-do-cliente) |
| [Get Lead](actions/get-lead.md) | `GET /:merchantAlias/leads/:id` | [docs](https://docs.yampi.com.br/api-reference/leads/visualizar-lead) |
| [Get Order](actions/get-order.md) | `GET /:merchantAlias/orders/:id` | [docs](https://docs.yampi.com.br/api-reference/pedidos/visualizar-detalhes-de-um-pedido) |
| [Get Product](actions/get-product.md) | `GET /:merchantAlias/public/catalog/products/:slug` | [docs](https://docs.yampi.com.br/api-reference/publico/catalogo/visualizar-informacoes-publicas-do-produto) |
| [List Brands](actions/list-brands.md) | `GET /:merchantAlias/catalog/brands` | [docs](https://docs.yampi.com.br/api-reference/catalogo/marcas/listar-marcas) |
| [List Categories](actions/list-categories.md) | `GET /:merchantAlias/catalog/categories` | [docs](https://docs.yampi.com.br/api-reference/catalogo/categorias/listar-categorias) |
| [List Category Products](actions/list-category-products.md) | `GET /:merchantAlias/catalog/categories/:id/products` | [docs](https://docs.yampi.com.br/api-reference/catalogo/categorias/listar-produtos-associados-a-uma-categoria) |
| [List Checkout Config](actions/list-checkout-config.md) | `GET /:merchantAlias/config/checkout` | [docs](https://docs.yampi.com.br/api-reference/configuracoes/checkout/listar-configuracao-do-checkout) |
| [List Customer Addresses](actions/list-customer-addresses.md) | `GET /:merchantAlias/customers/:customerId/addresses` | [docs](https://docs.yampi.com.br/api-reference/clientes/enderecos/listar-enderecos-de-um-cliente) |
| [List Customer Carts](actions/list-customer-carts.md) | `GET /:merchantAlias/customers/:id/carts` | [docs](https://docs.yampi.com.br/api-reference/clientes/listar-carrinhos-abandonados-de-um-cliente) |
| [List Customer Filters](actions/list-customer-filters.md) | `GET /:merchantAlias/customers/filters` | [docs](https://docs.yampi.com.br/api-reference/clientes/listar-filtros-de-busca-de-clientes) |
| [List Customers](actions/list-customers.md) | `GET /:merchantAlias/customers` | [docs](https://docs.yampi.com.br/api-reference/clientes/introduction) |
| [List Customizations](actions/list-customizations.md) | `GET /:merchantAlias/catalog/customizations` | [docs](https://docs.yampi.com.br/api-reference/catalogo/customizacoes/listar-customizacoes) |
| [List Lead Filters](actions/list-lead-filters.md) | `GET /:merchantAlias/leads/filters` | [docs](https://docs.yampi.com.br/api-reference/leads/listar-filtros-de-busca-dos-leads) |
| [List Leads](actions/list-leads.md) | `GET /:merchantAlias/leads` | [docs](https://docs.yampi.com.br/api-reference/leads/listar-leads) |
| [List Order Addresses](actions/list-order-addresses.md) | `GET /:merchantAlias/orders/:orderId/addresses` | [docs](https://docs.yampi.com.br/api-reference/pedidos/enderecos/listar-enderecos-de-um-pedido) |
| [List Order Filters](actions/list-order-filters.md) | `GET /:merchantAlias/orders/filters` | [docs](https://docs.yampi.com.br/api-reference/pedidos/pedido/listar-filtros-de-busca-de-pedidos) |
| [List Order Items](actions/list-order-items.md) | `GET /:merchantAlias/orders/:id/items` | [docs](https://docs.yampi.com.br/api-reference/pedidos/pedido/listar-produtos-de-um-pedido) |
| [List Order Tracking](actions/list-order-tracking.md) | `GET /:merchantAlias/orders/:id/tracking` | [docs](https://docs.yampi.com.br/api-reference/pedidos/rastreamento/rastrear-pedido) |
| [List Orders](actions/list-orders.md) | `GET /:merchantAlias/orders` | [docs](https://docs.yampi.com.br/api-reference/pedidos/pedido/listar-pedidos) |
| [List Product Combos](actions/list-product-combos.md) | `GET /:merchantAlias/catalog/products/:id/combos` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-combos-de-um-produto) |
| [List Product Comments](actions/list-product-comments.md) | `GET /:merchantAlias/catalog/comments` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/comentarios-de-produtos/listar-comentarios-de-produtos) |
| [List Product Promotions](actions/list-product-promotions.md) | `GET /:merchantAlias/catalog/products/:id/promotions` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-promocoes-que-um-produto-pertence) |
| [List Product Reviews](actions/list-product-reviews.md) | `GET /:merchantAlias/catalog/products/:id/reviews` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-avaliacoes-de-um-produto) |
| [List Product SKUs](actions/list-product-skus.md) | `GET /:merchantAlias/catalog/products/:id/skus` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-skus-de-um-produto) |
| [List Product Stocks](actions/list-product-stocks.md) | `GET /:merchantAlias/catalog/products/:id/stocks` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-estoques-de-todos-os-skus-de-um-produto) |
| [List Products](actions/list-products.md) | `GET /:merchantAlias/catalog/products` | [docs](https://docs.yampi.com.br/api-reference/catalogo/produtos/listar-produtos) |
