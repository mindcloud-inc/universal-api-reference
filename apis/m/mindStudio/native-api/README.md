# MindStudio: Native API Reference

A consolidated summary of MindStudio's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://university.mindstudio.ai/docs/developers/api-reference
- **API base URL:** `https://api.mindstudio.ai/developer/v2`

## Authentication

### API Key

Authenticate with a MindStudio developer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://university.mindstudio.ai/docs/developers/npm-package)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Signed Access URL](actions/generate-signed-access-url.md) | `POST /generate-signed-access-url` | [docs](https://university.mindstudio.ai/docs/deployment-of-ai-agents/embedding-ai-agents#getting-the-signed-url) |
| [Load App](actions/load-app.md) | `GET /apps/load` | [docs](https://university.mindstudio.ai/docs/developers/api-reference#load-an-app) |
| [Run App](actions/run-app.md) | `POST /apps/run` | [docs](https://university.mindstudio.ai/docs/developers/api-reference#run-an-app) |
