# Resemble: Native API Reference

A consolidated summary of Resemble's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.resemble.ai/welcome
- **OpenAPI specification:** https://docs.resemble.ai/openapi.json
- **API base URL:** `https://app.resemble.ai/api/v2`

## Authentication

### API Key

Use a Resemble API token. MindCloud stores it as credentials.apiKey and sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.resemble.ai/getting-started/authentication)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.resemble.ai/api-reference/projects/list-projects) |
