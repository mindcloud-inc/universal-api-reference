# Invoiless: Native API Reference

A consolidated summary of Invoiless's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.invoiless.com/guide/
- **API base URL:** `https://api.invoiless.com/v1`

## Authentication

### API Key

Connect with your Invoiless API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://docs.invoiless.com/guide/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `docs`. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.invoiless.com/guide/customers.html) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://docs.invoiless.com/guide/invoices.html) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:id` | [docs](https://docs.invoiless.com/guide/customers.html) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE /invoices/:id` | [docs](https://docs.invoiless.com/guide/invoices.html) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://docs.invoiless.com/guide/customers.html) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://docs.invoiless.com/guide/invoices.html) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.invoiless.com/guide/customers.html) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://docs.invoiless.com/guide/invoices.html) |
| [Send Invoice](actions/send-invoice.md) | `POST /invoices/:id/send` | [docs](https://docs.invoiless.com/guide/invoices.html) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://docs.invoiless.com/guide/customers.html) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://docs.invoiless.com/guide/invoices.html) |
