# SalesDrive: Native API Reference

A consolidated summary of SalesDrive's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://salesdrive.com.ua/knowledge/api/
- **OpenAPI specification:** https://api.salesdrive.me/swagger/openapi-uk.php
- **API base URL:** `https://{account}.salesdrive.me`

## Authentication

### SalesDrive API Keys

Connect SalesDrive with the account subdomain, Database API Key, and Account API Key.

### Credentials

- **API Key:** `apiKey` · required
- **Account Subdomain:** `account` · required · The SalesDrive account subdomain only, for example `demo` from `https://demo.salesdrive.me`.
- **Account API Key:** `accountApiKey` · required · SalesDrive Account API Key for payment and document-list APIs. This is separate from the Database API Key stored in the standard API Key field.

Send these headers with each API request:

```http
Form-Api-Key: <apiKey>
Account-Api-Key: <accountApiKey>
```

[Official authentication documentation](https://salesdrive.com.ua/knowledge/api/)

## API conventions

Responses from this API use JSON. The total page count is read from `pagination.pageCount`. The current page number is read from `pagination.currentPage`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Order Note](actions/add-order-note.md) | `POST /api/order/note/` | [docs](https://api.salesdrive.me/api/docs/#/order/order-note) |
| [Create Order](actions/create-order.md) | `POST /handler/` | [docs](https://api.salesdrive.me/api/docs/#/order/order-create) |
| [Get Manager By Phone Number](actions/get-manager-by-phone-number.md) | `GET /api/get_manager_by_phone_number/` | [docs](https://api.salesdrive.me/api/docs/#/call/call-manager) |
| [List Acts](actions/list-acts.md) | `GET /api/act/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/act-list) |
| [List Cash Orders](actions/list-cash-orders.md) | `GET /api/cash-order/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/cash-order-list) |
| [List Checks](actions/list-checks.md) | `GET /api/check/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/check-list) |
| [List Contracts](actions/list-contracts.md) | `GET /api/contract/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/contract-list) |
| [List Currency Rates](actions/list-currency-rates.md) | `GET /api/currencies/` | [docs](https://api.salesdrive.me/api/docs/#/currency/currency-list) |
| [List Delivery Methods](actions/list-delivery-methods.md) | `GET /api/delivery-methods/` | [docs](https://api.salesdrive.me/api/docs/#/order-field/delivery-method-list) |
| [List Invoices](actions/list-invoices.md) | `GET /api/invoice/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/invoice-list) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /api/statuses/` | [docs](https://api.salesdrive.me/api/docs/#/order-field/status-list) |
| [List Orders](actions/list-orders.md) | `GET /api/order/list/` | [docs](https://api.salesdrive.me/api/docs/#/order/order-list) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /api/payment-methods/` | [docs](https://api.salesdrive.me/api/docs/#/order-field/payment-method-list) |
| [List Payments](actions/list-payments.md) | `GET /api/payment/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/payment-list) |
| [List Product Arrivals](actions/list-product-arrivals.md) | `GET /api/arrival-product/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/arrival-product-list) |
| [List Sales Invoices](actions/list-sales-invoices.md) | `GET /api/sales-invoice/list/` | [docs](https://api.salesdrive.me/api/docs/#/document/sales-invoice-list) |
| [Update Currency Rates](actions/update-currency-rates.md) | `POST /api/currencies/` | [docs](https://api.salesdrive.me/api/docs/#/currency/currency-update) |
| [Update Order](actions/update-order.md) | `POST /api/order/update/` | [docs](https://api.salesdrive.me/api/docs/#/order/order-update) |
| [Upsert Categories](actions/upsert-categories.md) | `POST /category-handler/` | [docs](https://api.salesdrive.me/api/docs/#/product-category/category-update) |
| [Upsert Products](actions/upsert-products.md) | `POST /product-handler/` | [docs](https://api.salesdrive.me/api/docs/#/product-category/product-update) |
