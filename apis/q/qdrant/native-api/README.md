# Qdrant: Native API Reference

A consolidated summary of Qdrant's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.qdrant.tech/api-reference
- **API base URL:** `{baseUrl}`

## Authentication

### API Key

Authenticate Qdrant with a database API key and cluster URL.

### Credentials

- **API Key:** `apiKey` · required
- **Cluster URL:** `baseUrl` · required · Your Qdrant cluster URL. Paste the HTTPS cluster endpoint without a trailing slash.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://qdrant.tech/documentation/cloud/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://api.qdrant.tech/api-reference/collections/get-collections) |
