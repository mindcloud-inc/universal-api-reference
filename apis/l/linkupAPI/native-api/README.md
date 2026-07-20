# LinkupAPI: Native API Reference

A consolidated summary of LinkupAPI's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.linkup.so/pages/documentation/get-started/introduction
- **OpenAPI specification:** https://api.linkup.so/v1/openapi.json
- **API base URL:** `https://api.linkup.so/v1`

## Authentication

### API Key

Authenticate Linkup with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.linkup.so/pages/documentation/development/authentication)

## API conventions

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Research Task](actions/create-research-task.md) | `POST /research` | [docs](https://docs.linkup.so/pages/documentation/api-reference/endpoint/post-research) |
| [Fetch Page](actions/fetch-page.md) | `POST /fetch` | [docs](https://docs.linkup.so/pages/documentation/api-reference/endpoint/post-fetch) |
| [Generate Response](actions/generate-response.md) | `POST /responses` | [docs](https://api.linkup.so/v1/openapi.json) |
| [Get Credits Balance](actions/get-credits-balance.md) | `GET /credits/balance` | [docs](https://docs.linkup.so/pages/documentation/api-reference/endpoint/get-balance) |
| [Get Research Task](actions/get-research-task.md) | `GET /research/:id` | [docs](https://docs.linkup.so/pages/documentation/api-reference/endpoint/get-research-id) |
| [List Research Tasks](actions/list-research-tasks.md) | `GET /research` | [docs](https://docs.linkup.so/pages/documentation/api-reference/endpoint/get-research) |
| [Search](actions/search.md) | `POST /search` | [docs](https://docs.linkup.so/pages/documentation/api-reference/endpoint/post-search) |
