# Salescamp: Native API Reference

A consolidated summary of Salescamp's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developer.salescamp.app/reference/api-reference
- **API base URL:** `https://api.salescamp.app`

## Authentication

### API Key

Connect with a Salescamp API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.salescamp.app/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Activity to Item](actions/add-activity-to-item.md) | `POST /v1/collections/:collectionId/items/:itemId/activities` | [docs](https://developer.salescamp.app/reference/api-reference/activity) |
| [Create Company](actions/create-company.md) | `POST /v1/collections/69cd24c2f24a3ccfd974811e/items` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Create Deal](actions/create-deal.md) | `POST /v1/collections/69cd24c3f24a3ccfd974bb19/items` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Create Item](actions/create-item.md) | `POST /v1/collections/:collectionId/items` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Get Company](actions/get-company.md) | `GET /v1/collections/69cd24c2f24a3ccfd974811e/items/:itemId` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Get Deal](actions/get-deal.md) | `GET /v1/collections/69cd24c3f24a3ccfd974bb19/items/:itemId` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Get Item](actions/get-item.md) | `GET /v1/collections/:collectionId/items/:itemId` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [List Collections](actions/list-collections.md) | `GET /v1/collections` | [docs](https://developer.salescamp.app/reference/api-reference) |
| [Update Company](actions/update-company.md) | `PUT /v1/collections/69cd24c2f24a3ccfd974811e/items/:itemId` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Update Deal](actions/update-deal.md) | `PUT /v1/collections/69cd24c3f24a3ccfd974bb19/items/:itemId` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
| [Update Item](actions/update-item.md) | `PUT /v1/collections/:collectionId/items/:itemId` | [docs](https://developer.salescamp.app/reference/api-reference/items) |
