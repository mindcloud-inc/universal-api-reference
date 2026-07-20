# Digistore24: Native API Reference

A consolidated summary of Digistore24's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://dev.digistore24.com/hc/en-us/articles/38492246374673-API-reference-A-Z
- **API base URL:** `https://www.digistore24.com/api/call`

## Authentication

### API Key

Use a Digistore24 API key in the X-DS-API-KEY header without bearer Authorization injection.

### Credentials

- **API Key:** `apiKey` · required · Digistore24 API key sent in the X-DS-API-KEY header.

Send these headers with each API request:

```http
X-DS-API-KEY: <apiKey>
```

[Official authentication documentation](https://dev.digistore24.com/hc/en-us/articles/32479630493585-API-basics)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data.purchase_list`. The total page count is read from `data.page_count`. The current page number is read from `data.page_no`.

## Pagination

Use `page_size` in the query string to set the page size. Use `page_no` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Buy URL](actions/create-buy-url.md) | `POST /createBuyUrl` | [docs](https://digistore24.com/api/docs/paths/createBuyUrl.yaml) |
| [Create Payment Plan](actions/create-payment-plan.md) | `POST /createPaymentplan` | [docs](https://digistore24.com/api/docs/paths/createPaymentplan.yaml) |
| [Create Product](actions/create-product.md) | `POST /createProduct` | [docs](https://digistore24.com/api/docs/paths/createProduct.yaml) |
| [Get Purchase](actions/get-purchase.md) | `GET /getPurchase` | [docs](https://digistore24.com/api/docs/paths/getPurchase.yaml) |
| [List Buy URLs](actions/list-buy-urls.md) | `GET /listBuyUrls` | [docs](https://digistore24.com/api/docs/paths/listBuyUrls.yaml) |
| [List Commissions](actions/list-commissions.md) | `GET /listCommissions` | [docs](https://digistore24.com/api/docs/paths/listCommissions.yaml) |
| [List Invoices](actions/list-invoices.md) | `GET /listInvoices` | [docs](https://digistore24.com/api/docs/paths/listInvoices.yaml) |
| [List Payment Plans](actions/list-payment-plans.md) | `GET /listPaymentPlans` | [docs](https://digistore24.com/api/docs/paths/listPaymentPlans.yaml) |
| [List Payouts](actions/list-payouts.md) | `GET /listPayouts` | [docs](https://digistore24.com/api/docs/paths/listPayouts.yaml) |
| [List Product Groups](actions/list-product-groups.md) | `GET /listProductGroups` | [docs](https://digistore24.com/api/docs/paths/listProductGroups.yaml) |
| [List Products](actions/list-products.md) | `GET /listProducts` | [docs](https://digistore24.com/api/docs/paths/listProducts.yaml) |
| [List Purchases](actions/list-purchases.md) | `GET /listPurchases` | [docs](https://digistore24.com/api/docs/paths/listPurchases.yaml) |
| [List Transactions](actions/list-transactions.md) | `POST /listTransactions` | [docs](https://digistore24.com/api/docs/paths/listTransactions.yaml) |
| [List Vouchers](actions/list-vouchers.md) | `POST /listVouchers` | [docs](https://digistore24.com/api/docs/paths/listVouchers.yaml) |
| [Refund Partially](actions/refund-partially.md) | `POST /refundPartially` | [docs](https://digistore24.com/api/docs/paths/refundPartially.yaml) |
| [Refund Purchase](actions/refund-purchase.md) | `POST /refundPurchase` | [docs](https://digistore24.com/api/docs/paths/refundPurchase.yaml) |
| [Refund Transaction](actions/refund-transaction.md) | `POST /refundTransaction` | [docs](https://digistore24.com/api/docs/paths/refundTransaction.yaml) |
| [Start Rebilling](actions/start-rebilling.md) | `POST /startRebilling` | [docs](https://digistore24.com/api/docs/paths/startRebilling.yaml) |
| [Stop Rebilling](actions/stop-rebilling.md) | `POST /stopRebilling` | [docs](https://digistore24.com/api/docs/paths/stopRebilling.yaml) |
| [Update Buyer](actions/update-buyer.md) | `PUT /updateBuyer` | [docs](https://digistore24.com/api/docs/paths/updateBuyer.yaml) |
| [Update Payment Plan](actions/update-payment-plan.md) | `PUT /updatePaymentplan` | [docs](https://digistore24.com/api/docs/paths/updatePaymentplan.yaml) |
| [Update Product](actions/update-product.md) | `PUT /updateProduct` | [docs](https://digistore24.com/api/docs/paths/updateProduct.yaml) |
| [Update Product Group](actions/update-product-group.md) | `PUT /updateProductGroup` | [docs](https://digistore24.com/api/docs/paths/updateProductGroup.yaml) |
| [Update Purchase](actions/update-purchase.md) | `PUT /updatePurchase` | [docs](https://digistore24.com/api/docs/paths/updatePurchase.yaml) |
