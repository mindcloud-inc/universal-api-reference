# Monetizze: Native API Reference

A consolidated summary of Monetizze's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.monetizze.com.br/2.1/apidoc/
- **API base URL:** `https://api.monetizze.com.br/2.1`

## Authentication

### API Key

Use your Monetizze API key from Ferramentas > API.

### Credentials

- **API Key:** `apiKey` · required
- **Token:** `token` · optional · Temporary Monetizze access token. Generate it with the access-token action; it expires after 15 minutes of inactivity.
- **Checkout API Key:** `checkoutApiKey` · optional · Optional Monetizze transparent-checkout API key used by checkout processing endpoints.

Send these headers with each API request:

```http
TOKEN: <token>
```

[Official authentication documentation](https://help.monetizze.com.br/books/integracoes/page/api-monetizze)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `pages`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Checkout Installments](actions/calculate-checkout-installments.md) | `POST https://app.monetizze.com.br/checkout/transparente/parcelamento` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Checkout_Transparente-Parcelamento) |
| [Generate Access Token](actions/generate-access-token.md) | `GET /token` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Security-Token) |
| [Generate Checkout Key](actions/generate-checkout-key.md) | `GET https://app.monetizze.com.br/checkout/transparente/js` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Checkout_Transparente-CTKEY) |
| [Process Transparent Checkout Order](actions/process-transparent-checkout-order.md) | `POST https://app.monetizze.com.br/checkout/transparente/processar` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Checkout_Transparente-Tracking) |
| [Save Ecommerce Checkout](actions/save-ecommerce-checkout.md) | `POST /ecommerce/checkout` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Ecommerce-PostProdutos) |
| [Search Transactions](actions/search-transactions.md) | `GET /transactions` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Geral-Transactions) |
| [Update Boleto Due Date](actions/update-boleto-due-date.md) | `POST /boleto` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Produtor-Boleto) |
| [Update Sales Tracking](actions/update-sales-tracking.md) | `POST /sales/tracking` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Produtor-Tracking) |
| [Update Subscription Plan](actions/update-subscription-plan.md) | `POST /assinatura/atualizar` | [docs](https://api.monetizze.com.br/2.1/apidoc/#api-Assinatura-Atualizar_Assinatura) |
