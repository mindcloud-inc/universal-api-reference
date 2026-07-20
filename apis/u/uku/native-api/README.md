# Uku: Native API Reference

A consolidated summary of Uku's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.getuku.com/docs/
- **OpenAPI specification:** https://app.getuku.com/docs/sandbox/api.json
- **API base URL:** `https://app.getuku.com/api/v1.0`

## Authentication

### JWT Login (API Key + Secret)

Use your Uku API key and API secret to mint a bearer token through the documented login endpoint.

### Credentials

- **API Secret:** `apiSecret` · required · The Uku API secret generated alongside the API key in Public API settings.
- **API Key:** `apiKey` · required · The Uku API key generated in Settings -> Apps -> Public API.

Send these headers with each API request:

```http
Authorization: Bearer <custom.data.token>
```

[Official authentication documentation](https://help.getuku.com/en/articles/10147875-public-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://app.getuku.com/docs/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://app.getuku.com/docs/) |
| [Get Client](actions/get-client.md) | `GET /clients/:clientId` | [docs](https://app.getuku.com/docs/) |
| [Get Client Field](actions/get-client-field.md) | `GET /client_fields/:clientFieldId` | [docs](https://app.getuku.com/docs/) |
| [Get Client Group](actions/get-client-group.md) | `GET /client_groups/:clientGroupId` | [docs](https://app.getuku.com/docs/) |
| [Get Invoice Seller](actions/get-invoice-seller.md) | `GET /invoice_sellers/:invoiceSellerId` | [docs](https://app.getuku.com/docs/) |
| [Get Member](actions/get-member.md) | `GET /members/:memberId` | [docs](https://app.getuku.com/docs/) |
| [Get Member Group](actions/get-member-group.md) | `GET /member_groups/:memberGroupId` | [docs](https://app.getuku.com/docs/) |
| [Get Topic](actions/get-topic.md) | `GET /topics/:topicId` | [docs](https://app.getuku.com/docs/) |
| [List Client Fields](actions/list-client-fields.md) | `GET /client_fields` | [docs](https://app.getuku.com/docs/) |
| [List Client Groups](actions/list-client-groups.md) | `GET /client_groups` | [docs](https://app.getuku.com/docs/) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://app.getuku.com/docs/) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://app.getuku.com/docs/) |
| [List Invoice Sellers](actions/list-invoice-sellers.md) | `GET /invoice_sellers` | [docs](https://app.getuku.com/docs/) |
| [List Member Groups](actions/list-member-groups.md) | `GET /member_groups` | [docs](https://app.getuku.com/docs/) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://app.getuku.com/docs/) |
| [List Product Fields](actions/list-product-fields.md) | `GET /product_fields` | [docs](https://app.getuku.com/docs/) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://app.getuku.com/docs/) |
| [List Task Fields](actions/list-task-fields.md) | `GET /task_fields` | [docs](https://app.getuku.com/docs/) |
| [List Topics](actions/list-topics.md) | `GET /topics` | [docs](https://app.getuku.com/docs/) |
