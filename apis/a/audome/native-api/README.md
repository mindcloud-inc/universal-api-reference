# Audome: Native API Reference

A consolidated summary of Audome's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://app.audome.com/api-documentation
- **OpenAPI specification:** https://app.audome.com/api-documentation.openapi
- **API base URL:** `https://app.audome.com/api/v1`

## Authentication

### API Key (Bearer Token)

Use a long-lived bearer token generated via POST /api/v1/authenticate and pass it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required
- **Bearer Token:** `accessToken` · required · Long-lived bearer token for Audome API. Enter full value as 'Bearer <token>' exactly as required for the Authorization header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.audome.com/api-documentation)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client Project](actions/create-client-project.md) | `POST /client-projects` | [docs](https://app.audome.com/api-documentation) |
| [Create Tag List](actions/create-tag-list.md) | `POST /tag-lists` | [docs](https://app.audome.com/api-documentation#endpoints-POSTapi-v1-tag-lists) |
| [Delete Tag List](actions/delete-tag-list.md) | `DELETE /tag-lists/:taglistUuid` | [docs](https://app.audome.com/api-documentation#endpoints-DELETEapi-v1-tag-lists--taglistUuid-) |
| [Get Client Project](actions/get-client-project.md) | `GET /client-projects/:uuid` | [docs](https://app.audome.com/api-documentation) |
| [Get Tag List](actions/get-tag-list.md) | `GET /tag-lists/:taglistUuid` | [docs](https://app.audome.com/api-documentation#endpoints-GETapi-v1-tag-lists--taglistUuid-) |
| [List Client Projects](actions/list-client-projects.md) | `GET /client-projects` | [docs](https://app.audome.com/api-documentation) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://app.audome.com/api-documentation#endpoints-GETapi-v1-projects) |
| [List Tag Lists](actions/list-tag-lists.md) | `GET /tag-lists` | [docs](https://app.audome.com/api-documentation#endpoints-GETapi-v1-tag-lists) |
| [Update Tag List](actions/update-tag-list.md) | `PATCH /tag-lists/:taglistUuid` | [docs](https://app.audome.com/api-documentation#endpoints-PATCHapi-v1-tag-lists--taglistUuid-) |
