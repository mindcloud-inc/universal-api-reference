# SalesapCRM: Native API Reference

A consolidated summary of SalesapCRM's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.salesap.ru/
- **API base URL:** `https://app.salesap.ru/api/v1`

## Authentication

### API Key

Use a SalesapCRM API token in the Authorization header as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://salesap.ru/help/info/integratsiya-s-salesapcrm-po-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.page-count`.

## Pagination

Use `page[size]` in the query string to set the page size (default 50; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://api.salesap.ru/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.salesap.ru/) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://api.salesap.ru/) |
| [Create Diary Event](actions/create-diary-event.md) | `POST /diary-events` | [docs](https://api.salesap.ru/) |
| [Create Diary Task](actions/create-diary-task.md) | `POST /diary-tasks` | [docs](https://api.salesap.ru/) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://api.salesap.ru/) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://api.salesap.ru/) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://api.salesap.ru/) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/{id}` | [docs](https://api.salesap.ru/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{id}` | [docs](https://api.salesap.ru/) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /deals/{id}` | [docs](https://api.salesap.ru/) |
| [Delete Diary Event](actions/delete-diary-event.md) | `DELETE /diary-events/{id}` | [docs](https://api.salesap.ru/) |
| [Delete Diary Task](actions/delete-diary-task.md) | `DELETE /diary-tasks/{id}` | [docs](https://api.salesap.ru/) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/{id}` | [docs](https://api.salesap.ru/) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/{id}` | [docs](https://api.salesap.ru/) |
| [Get Company](actions/get-company.md) | `GET /companies/{id}` | [docs](https://api.salesap.ru/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{id}` | [docs](https://api.salesap.ru/) |
| [Get Current Token](actions/get-current-token.md) | `GET /current-token` | [docs](https://api.salesap.ru/) |
| [Get Deal](actions/get-deal.md) | `GET /deals/{id}` | [docs](https://api.salesap.ru/) |
| [Get Diary Event](actions/get-diary-event.md) | `GET /diary-events/{id}` | [docs](https://api.salesap.ru/) |
| [Get Diary Task](actions/get-diary-task.md) | `GET /diary-tasks/{id}` | [docs](https://api.salesap.ru/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/{id}` | [docs](https://api.salesap.ru/) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://api.salesap.ru/) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://api.salesap.ru/) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://api.salesap.ru/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.salesap.ru/) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://api.salesap.ru/) |
| [List Diary Events](actions/list-diary-events.md) | `GET /diary-events` | [docs](https://api.salesap.ru/) |
| [List Diary Tasks](actions/list-diary-tasks.md) | `GET /diary-tasks` | [docs](https://api.salesap.ru/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://api.salesap.ru/) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://api.salesap.ru/) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://api.salesap.ru/) |
| [Update Company](actions/update-company.md) | `PATCH /companies/{id}` | [docs](https://api.salesap.ru/) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{id}` | [docs](https://api.salesap.ru/) |
| [Update Deal](actions/update-deal.md) | `PATCH /deals/{id}` | [docs](https://api.salesap.ru/) |
| [Update Diary Event](actions/update-diary-event.md) | `PATCH /diary-events/{id}` | [docs](https://api.salesap.ru/) |
| [Update Diary Task](actions/update-diary-task.md) | `PATCH /diary-tasks/{id}` | [docs](https://api.salesap.ru/) |
| [Update Invoice](actions/update-invoice.md) | `PATCH /invoices/{id}` | [docs](https://api.salesap.ru/) |
| [Update Order](actions/update-order.md) | `PATCH /orders/{id}` | [docs](https://api.salesap.ru/) |
| [Update Product](actions/update-product.md) | `PATCH /products/{id}` | [docs](https://api.salesap.ru/) |
