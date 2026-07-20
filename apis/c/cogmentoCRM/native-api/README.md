# Cogmento CRM: Native API Reference

A consolidated summary of Cogmento CRM's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.cogmento.com/api
- **OpenAPI specification:** https://api.cogmento.com/static/swagger/index.html
- **API base URL:** `https://api.freecrm.com/api/1`

## Authentication

### Cogmento API Token

Authenticate Cogmento API requests with an access token sent as `Authorization: Token {ACCESS_TOKEN}`.

### Credentials

- **Cogmento API Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.cogmento.com/hc/en-us/articles/25558877135885-Cogmento-API)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `start` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `filter`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts/` | [docs](https://api.cogmento.com/static/swagger/index.html#/Contacts/post_contacts_) |
| [Create Deal](actions/create-deal.md) | `POST /deals/` | [docs](https://api.cogmento.com/static/swagger/index.html#/Deals/post_deals_) |
| [Create Task](actions/create-task.md) | `POST /tasks/` | [docs](https://api.cogmento.com/static/swagger/index.html#/Tasks/post_tasks_) |
| [Get Current User](actions/get-current-user.md) | `GET /auth/user` | [docs](https://api.cogmento.com/static/swagger/index.html) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://api.cogmento.com/static/swagger/index.html#/Contacts/get_contacts_) |
| [List Deals](actions/list-deals.md) | `GET /deals/` | [docs](https://api.cogmento.com/static/swagger/index.html#/Deals/get_deals_) |
| [List Products](actions/list-products.md) | `GET /products/` | [docs](https://api.cogmento.com/static/swagger/index.html) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks/` | [docs](https://api.cogmento.com/static/swagger/index.html#/Tasks/get_tasks_) |
| [List Templates](actions/list-templates.md) | `GET /templates/` | [docs](https://help.cogmento.com/hc/en-us/articles/25558877135885-Cogmento-API) |
