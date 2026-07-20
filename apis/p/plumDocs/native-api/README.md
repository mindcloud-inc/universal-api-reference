# PlumDocs: Native API Reference

A consolidated summary of PlumDocs's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://plumdocs.com/api-docs
- **API base URL:** `https://plumdocs.com/api/zapier`

## Authentication

### API Key

Connect PlumDocs with an API key from Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://plumdocs.com/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Document](actions/generate-document.md) | `POST /workflows/:id/run` | [docs](https://plumdocs.com/api-docs) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /auth/test` | [docs](https://plumdocs.com/api-docs) |
| [Get Workflow Fields](actions/get-workflow-fields.md) | `GET /workflows/:id/fields` | [docs](https://plumdocs.com/api-docs) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://plumdocs.com/api-docs) |
