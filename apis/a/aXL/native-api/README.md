# AXL: Native API Reference

A consolidated summary of AXL's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://axl.tech/developers/api
- **OpenAPI specification:** https://cdn.app.axl.tech/openapi/schemas/en.json
- **API base URL:** `https://app.axl.tech/api/v1`

## Authentication

### API Key

Authenticate with an AXL API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.axl.tech/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `take` in the query string to set the page size (default 50). Use `skip` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Certificates](actions/get-certificates.md) | `GET /cert` | [docs](https://app.axl.tech/api/public) |
| [Get Contact](actions/get-contact.md) | `GET /crm/lead/:id` | [docs](https://app.axl.tech/api/public) |
| [Get Contacts](actions/get-contacts.md) | `POST /crm/lead/table` | [docs](https://app.axl.tech/api/public) |
| [Get Course Categories](actions/get-course-categories.md) | `GET /course-category` | [docs](https://app.axl.tech/api/public) |
| [Get Courses](actions/get-courses.md) | `GET /course` | [docs](https://app.axl.tech/api/public) |
| [Get Libraries](actions/get-libraries.md) | `GET /library` | [docs](https://app.axl.tech/api/public) |
| [Get Orders](actions/get-orders.md) | `POST /purchase-order/list` | [docs](https://app.axl.tech/api/public) |
| [Get Partner Transactions](actions/get-partner-transactions.md) | `GET /partnership/transaction` | [docs](https://app.axl.tech/api/public) |
| [Get Partnership Members](actions/get-partnership-members.md) | `GET /partnership/member` | [docs](https://app.axl.tech/api/public) |
| [Get Payments](actions/get-payments.md) | `GET /purchase-payment` | [docs](https://app.axl.tech/api/public) |
| [Get Products](actions/get-products.md) | `GET /product` | [docs](https://app.axl.tech/api/public) |
| [Get Tasks](actions/get-tasks.md) | `GET /task-verification` | [docs](https://app.axl.tech/api/public) |
