# ActiveMerge: Native API Reference

A consolidated summary of ActiveMerge's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://app.activemerge.com/api/documentation
- **OpenAPI specification:** https://app.activemerge.com/docs?api-docs.json
- **API base URL:** `https://app.activemerge.com`

## Authentication

### API Key

Use your ActiveMerge API key in the API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
API-KEY: <apiKey>
```

[Official authentication documentation](https://app.activemerge.com/api/documentation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Document](actions/generate-document.md) | `POST /api/document-generation/generate` | [docs](https://app.activemerge.com/api/documentation) |
| [Generate Workflow Documents](actions/generate-workflow-documents.md) | `POST /api/workflows/generate` | [docs](https://app.activemerge.com/api/documentation) |
| [Get User Credits](actions/get-user-credits.md) | `GET /api/user/credits` | [docs](https://app.activemerge.com/api/documentation) |
| [List Files](actions/list-files.md) | `GET /api/files` | [docs](https://app.activemerge.com/api/documentation) |
| [List Image Templates](actions/list-image-templates.md) | `GET /api/image-templates` | [docs](https://app.activemerge.com/api/documentation) |
| [List Templates](actions/list-templates.md) | `GET /api/templates` | [docs](https://app.activemerge.com/api/documentation) |
| [List Workflows](actions/list-workflows.md) | `GET /api/workflows` | [docs](https://app.activemerge.com/api/documentation) |
