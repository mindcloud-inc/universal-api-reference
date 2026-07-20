# Lome: Native API Reference

A consolidated summary of Lome's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://grow.withlome.com/articles/lome/api
- **API base URL:** `https://grow.withlome.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Your Lome Account ID from Settings > API.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://grow.withlome.com/articles/lome/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://grow.withlome.com/articles/lome/api) |
| [List Communities](actions/list-communities.md) | `GET /v1/communities` | [docs](https://grow.withlome.com/articles/lome/api) |
| [List Recent Community Responses](actions/list-recent-community-responses.md) | `GET /v1/new-community-responses/recent` | [docs](https://grow.withlome.com/articles/lome/api) |
| [List Recent Responses](actions/list-recent-responses.md) | `GET /v1/webhook/new-response/recent` | [docs](https://grow.withlome.com/articles/lome/api) |
