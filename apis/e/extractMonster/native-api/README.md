# Extract Monster: Native API Reference

A consolidated summary of Extract Monster's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://extract.monster/docs
- **OpenAPI specification:** https://api.extract.monster/openapi.json
- **API base URL:** `https://api.extract.monster`

## Authentication

### API Key

Use an Extract Monster API key. The provider accepts bearer authentication and the MindCloud native apiKey runtime injects Authorization: Bearer {{credentials.apiKey}}.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://extract.monster/docs)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract Data From Bytes](actions/extract-data-from-bytes.md) | `POST /v1/extract/bytes` | [docs](https://api.extract.monster/openapi.json) |
| [Extract Data From File](actions/extract-data-from-file.md) | `POST /v1/extract/file` | [docs](https://api.extract.monster/openapi.json) |
| [Extract Data From Text](actions/extract-data-from-text.md) | `POST /v1/extract/text` | [docs](https://api.extract.monster/openapi.json) |
| [Get API Info](actions/get-api-info.md) | `GET /` | [docs](https://api.extract.monster/openapi.json) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://api.extract.monster/openapi.json) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://api.extract.monster/openapi.json) |
