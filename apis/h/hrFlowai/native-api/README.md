# HrFlow.ai: Native API Reference

A consolidated summary of HrFlow.ai's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://developers.hrflow.ai/docs/api-overview
- **API base URL:** `https://api.hrflow.ai`

## Authentication

### API Key

Use an HrFlow.ai secret key together with the account email address that owns the key.

### Credentials

- **API Key:** `apiKey` · required
- **User Email:** `userEmail` · required · The HrFlow.ai account email address associated with the selected API key.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
X-USER-EMAIL: <userEmail>
```

[Official authentication documentation](https://developers.hrflow.ai/docs/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | `GET /v1/boards` | [docs](https://developers.hrflow.ai/reference/boards-searching) |
| [List Sources](actions/list-sources.md) | `GET /v1/sources` | [docs](https://developers.hrflow.ai/reference/sources-searching) |
| [List Workflows](actions/list-workflows.md) | `GET /v1/workflows` | [docs](https://developers.hrflow.ai/reference/workflows-searching) |
| [Validate Credentials](actions/validate-credentials.md) | `GET /v1/auth` | [docs](https://developers.hrflow.ai/docs/api-authentication) |
