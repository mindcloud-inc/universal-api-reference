# Conta Azul: Native API Reference

A consolidated summary of Conta Azul's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developers.contaazul.com/auth
- **OpenAPI specification:** https://developers.contaazul.com/open-api-docs/open-api-person
- **API base URL:** `https://api-v2.contaazul.com`

## Authentication

### OAuth 2.0

Conta Azul OAuth 2.0 Authorization Code flow for ERP tenants.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.contaazul.com/login to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.contaazul.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile aws.cognito.signin.user.admin`.

Refresh expired access tokens with a POST request to https://auth.contaazul.com/oauth2/token.

[Official authentication documentation](https://developers.contaazul.com/auth)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Acquittance](actions/get-acquittance.md) | `GET /v1/financeiro/eventos-financeiros/parcelas/baixa/{baixa_id}` | [docs](https://developers.contaazul.com/open-api-docs/acquittance-apis-openapi) |
| [Get Connected Company](actions/get-connected-company.md) | `GET /v1/pessoas/conta-conectada` | [docs](https://developers.contaazul.com/open-api-docs/open-api-person) |
| [Get Financial Account Current Balance](actions/get-financial-account-current-balance.md) | `GET /v1/conta-financeira/{id_conta_financeira}/saldo-atual` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [Get Financial Installment](actions/get-financial-installment.md) | `GET /v1/financeiro/eventos-financeiros/parcelas/{id}` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [Get Invoice By Key](actions/get-invoice-by-key.md) | `GET /v1/notas-fiscais/{chave}` | [docs](https://developers.contaazul.com/open-api-docs/open-api-invoice) |
| [Get Next Contract Number](actions/get-next-contract-number.md) | `GET /v1/contratos/proximo-numero` | [docs](https://developers.contaazul.com/open-api-docs/contracts-apis-openapi) |
| [Get Next Sale Number](actions/get-next-sale-number.md) | `GET /v1/venda/proximo-numero` | [docs](https://developers.contaazul.com/open-api-docs/sales-apis-openapi) |
| [Get Person](actions/get-person.md) | `GET /v1/pessoas/{id}` | [docs](https://developers.contaazul.com/open-api-docs/open-api-person) |
| [Get Person By Legacy ID](actions/get-person-by-legacy-id.md) | `GET /v1/pessoas/legado/{id}` | [docs](https://developers.contaazul.com/open-api-docs/open-api-person) |
| [Get Product](actions/get-product.md) | `GET /v1/produtos/{id}` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [Get Sale](actions/get-sale.md) | `GET /v1/venda/{id}` | [docs](https://developers.contaazul.com/open-api-docs/sales-apis-openapi) |
| [Get Sale Printable](actions/get-sale-printable.md) | `GET /v1/venda/{id}/imprimir` | [docs](https://developers.contaazul.com/open-api-docs/sales-apis-openapi) |
| [List Acquittances By Installment](actions/list-acquittances-by-installment.md) | `GET /v1/financeiro/eventos-financeiros/parcelas/{parcela_id}/baixa` | [docs](https://developers.contaazul.com/open-api-docs/acquittance-apis-openapi) |
| [List Categories](actions/list-categories.md) | `GET /v1/categorias` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List Changed Financial Events](actions/list-changed-financial-events.md) | `GET /v1/financeiro/eventos-financeiros/alteracoes` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List Contracts](actions/list-contracts.md) | `GET /v1/contratos` | [docs](https://developers.contaazul.com/open-api-docs/contracts-apis-openapi) |
| [List Cost Centers](actions/list-cost-centers.md) | `GET /v1/centro-de-custo` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List DRE Categories](actions/list-dre-categories.md) | `GET /v1/financeiro/categorias-dre` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List Ecommerce Brands](actions/list-ecommerce-brands.md) | `GET /v1/produtos/ecommerce-marcas` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Ecommerce Categories](actions/list-ecommerce-categories.md) | `GET /v1/produtos/ecommerce-categorias` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Financial Accounts](actions/list-financial-accounts.md) | `GET /v1/conta-financeira` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List Financial Event Installments](actions/list-financial-event-installments.md) | `GET /v1/financeiro/eventos-financeiros/{id_evento}/parcelas` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List Financial Transfers](actions/list-financial-transfers.md) | `GET /v1/financeiro/transferencias` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List Invoices](actions/list-invoices.md) | `GET /v1/notas-fiscais` | [docs](https://developers.contaazul.com/open-api-docs/open-api-invoice) |
| [List Opening Balances](actions/list-opening-balances.md) | `GET /v1/financeiro/eventos-financeiros/saldo-inicial` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [List People](actions/list-people.md) | `GET /v1/pessoas` | [docs](https://developers.contaazul.com/open-api-docs/open-api-person) |
| [List Product Categories](actions/list-product-categories.md) | `GET /v1/produtos/categorias` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Product CESTs](actions/list-product-cests.md) | `GET /v1/produtos/cest` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Product NCMs](actions/list-product-ncms.md) | `GET /v1/produtos/ncm` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Product Units Of Measure](actions/list-product-units-of-measure.md) | `GET /v1/produtos/unidades-medida` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Products](actions/list-products.md) | `GET /v1/produtos` | [docs](https://developers.contaazul.com/open-api-docs/open-api-inventory) |
| [List Sale Items](actions/list-sale-items.md) | `GET /v1/venda/{id_venda}/itens` | [docs](https://developers.contaazul.com/open-api-docs/sales-apis-openapi) |
| [List Salespeople](actions/list-salespeople.md) | `GET /v1/venda/vendedores` | [docs](https://developers.contaazul.com/open-api-docs/sales-apis-openapi) |
| [List Service Invoices](actions/list-service-invoices.md) | `GET /v1/notas-fiscais-servico` | [docs](https://developers.contaazul.com/open-api-docs/open-api-invoice) |
| [Search Accounts Payable](actions/search-accounts-payable.md) | `GET /v1/financeiro/eventos-financeiros/contas-a-pagar/buscar` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [Search Accounts Receivable](actions/search-accounts-receivable.md) | `GET /v1/financeiro/eventos-financeiros/contas-a-receber/buscar` | [docs](https://developers.contaazul.com/open-api-docs/financial-apis-openapi) |
| [Search Sales](actions/search-sales.md) | `GET /v1/venda/busca` | [docs](https://developers.contaazul.com/open-api-docs/sales-apis-openapi) |
