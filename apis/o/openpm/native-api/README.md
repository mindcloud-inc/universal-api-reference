# openpm: Native API Reference

A consolidated summary of openpm's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://openpm.ai/apis/openpm
- **OpenAPI specification:** https://openpm.ai/packages/openpm/openapi.json
- **API base URL:** `https://openpm.ai/api`

## Authentication

### API Key

Authenticate OpenPM requests with an API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://openpm.ai/apis/openpm)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Package](actions/create-package.md) | `POST /packages` | [docs](https://openpm.ai/apis/openpm) |
| [Get Package](actions/get-package.md) | `GET /packages/:packageId` | [docs](https://openpm.ai/apis/openpm) |
| [Get Package AI Plugin Manifest](actions/get-package-ai-plugin-manifest.md) | `GET /packages/:packageId/ai-plugin` | [docs](https://openpm.ai/apis/openpm) |
| [Get Package OpenAPI Spec](actions/get-package-openapi-spec.md) | `GET /packages/:packageId/openapi` | [docs](https://openpm.ai/apis/openpm) |
| [List Connected Packages](actions/list-connected-packages.md) | `GET /packages/connected` | [docs](https://openpm.ai/apis/openpm) |
| [List Packages](actions/list-packages.md) | `GET /packages` | [docs](https://openpm.ai/apis/openpm) |
| [Lookup Packages](actions/lookup-packages.md) | `GET /packages/lookup` | [docs](https://openpm.ai/apis/openpm) |
| [Search Packages](actions/search-packages.md) | `GET /packages/search` | [docs](https://openpm.ai/apis/openpm) |
| [Update Package](actions/update-package.md) | `PUT /packages/:packageId` | [docs](https://openpm.ai/apis/openpm) |
