# SynergyCRM: Native API Reference

A consolidated summary of SynergyCRM's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.synergycrm.ru/
- **API base URL:** `https://app.synergycrm.ru/api/v1`

## Authentication

### API Token

Authenticate with a SynergyCRM API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://synergycrm.ru/help/api-synergy-crm)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size (default 50; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://api.synergycrm.ru/#companies) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api.synergycrm.ru/#contacts) |
| [Get Deal](actions/get-deal.md) | `GET /deals/:id` | [docs](https://api.synergycrm.ru/#deals) |
| [Get Deal Stage](actions/get-deal-stage.md) | `GET /deal-stages/:id` | [docs](https://api.synergycrm.ru/#deal-stages) |
| [Get Deal Stage Category](actions/get-deal-stage-category.md) | `GET /deal-stage-categories/:id` | [docs](https://api.synergycrm.ru/#deal-stage-categories) |
| [Get Deal Status](actions/get-deal-status.md) | `GET /deal-statuses/:id` | [docs](https://api.synergycrm.ru/#deal-statuses) |
| [Get Diary Task](actions/get-diary-task.md) | `GET /diary-tasks/:id` | [docs](https://api.synergycrm.ru/#diary-tasks) |
| [Get Entry](actions/get-entry.md) | `GET /entries/:id` | [docs](https://api.synergycrm.ru/#entries) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://api.synergycrm.ru/#orders) |
| [Get Order Status](actions/get-order-status.md) | `GET /order-statuses/:id` | [docs](https://api.synergycrm.ru/#order-statuses) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://api.synergycrm.ru/#products) |
| [Get Product Category](actions/get-product-category.md) | `GET /product-categories/:id` | [docs](https://api.synergycrm.ru/#product-categories) |
| [Get Product Status](actions/get-product-status.md) | `GET /product-statuses/:id` | [docs](https://api.synergycrm.ru/#product-statuses) |
| [Get Product Type](actions/get-product-type.md) | `GET /product-types/:id` | [docs](https://api.synergycrm.ru/#product-types) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://api.synergycrm.ru/#projects) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://api.synergycrm.ru/#companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.synergycrm.ru/#contacts) |
| [List Deal Stage Categories](actions/list-deal-stage-categories.md) | `GET /deal-stage-categories` | [docs](https://api.synergycrm.ru/#deal-stage-categories) |
| [List Deal Stages](actions/list-deal-stages.md) | `GET /deal-stages` | [docs](https://api.synergycrm.ru/#deal-stages) |
| [List Deal Statuses](actions/list-deal-statuses.md) | `GET /deal-statuses` | [docs](https://api.synergycrm.ru/#deal-statuses) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://api.synergycrm.ru/#deals) |
| [List Diary Tasks](actions/list-diary-tasks.md) | `GET /diary-tasks` | [docs](https://api.synergycrm.ru/#diary-tasks) |
| [List Entries](actions/list-entries.md) | `GET /entries` | [docs](https://api.synergycrm.ru/#entries) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /order-statuses` | [docs](https://api.synergycrm.ru/#order-statuses) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://api.synergycrm.ru/#orders) |
| [List Product Categories](actions/list-product-categories.md) | `GET /product-categories` | [docs](https://api.synergycrm.ru/#product-categories) |
| [List Product Statuses](actions/list-product-statuses.md) | `GET /product-statuses` | [docs](https://api.synergycrm.ru/#product-statuses) |
| [List Product Types](actions/list-product-types.md) | `GET /product-types` | [docs](https://api.synergycrm.ru/#product-types) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://api.synergycrm.ru/#products) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.synergycrm.ru/#projects) |
