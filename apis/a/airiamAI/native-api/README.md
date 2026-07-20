# Airiam AI: Native API Reference

A consolidated summary of Airiam AI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.ai.airiam.com/reference/getting-started-with-the-airiam-ai-restapi
- **API base URL:** `https://platform.sectorflow.ai`

## Authentication

### API Key

API key used as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ai.airiam.com/reference/getting-started-with-the-airiam-ai-restapi)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Model To Team](actions/add-model-to-team.md) | `POST /api/v1/models/add-to-team` | [docs](https://docs.ai.airiam.com/reference/models) |
| [Create Expert](actions/create-expert.md) | `POST /api/v1/plus` | [docs](https://docs.ai.airiam.com/reference/airiam-ai-experts) |
| [Create Model](actions/create-model.md) | `POST /api/v1/models` | [docs](https://docs.ai.airiam.com/reference/models) |
| [Create Workspace](actions/create-workspace.md) | `POST /api/v1/workspaces` | [docs](https://docs.ai.airiam.com/reference/workspaces) |
| [Delete Expert](actions/delete-expert.md) | `DELETE /api/v1/plus/:plusId` | [docs](https://docs.ai.airiam.com/reference/airiam-ai-experts) |
| [Delete Expert File](actions/delete-expert-file.md) | `DELETE /api/v1/plus/file/:fileId` | [docs](https://docs.ai.airiam.com/reference/airiam-ai-experts) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /api/v1/workspaces/:workspaceId` | [docs](https://docs.ai.airiam.com/reference/workspaces) |
| [Get All Models](actions/get-all-models.md) | `GET /api/v1/models/all` | [docs](https://docs.ai.airiam.com/reference/models) |
| [Get Chat History](actions/get-chat-history.md) | `GET /api/v1/chat/:workspaceId/history` | [docs](https://docs.ai.airiam.com/reference/chat) |
| [Get Expert](actions/get-expert.md) | `GET /api/v1/plus/:plusId` | [docs](https://docs.ai.airiam.com/reference/airiam-ai-experts) |
| [Get Expert File Content](actions/get-expert-file-content.md) | `GET /api/v1/plus/file/:fileId/content` | [docs](https://docs.ai.airiam.com/reference/airiam-ai-experts) |
| [Get Greeting](actions/get-greeting.md) | `GET /api/v1/chat/:workspaceId/greeting` | [docs](https://docs.ai.airiam.com/reference/chat) |
| [Get Model](actions/get-model.md) | `GET /api/v1/models/:baseModel` | [docs](https://docs.ai.airiam.com/reference/models) |
| [Get Sample Prompts](actions/get-sample-prompts.md) | `GET /api/v1/chat/:workspaceId/sample-prompts` | [docs](https://docs.ai.airiam.com/reference/chat) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/v1/workspaces/:workspaceId` | [docs](https://docs.ai.airiam.com/reference/workspaces) |
| [List All Models With Body](actions/list-all-models-post.md) | `POST /api/v1/models/list/all` | [docs](https://docs.ai.airiam.com/reference/models) |
| [List Experts](actions/list-experts.md) | `GET /api/v1/plus` | [docs](https://docs.ai.airiam.com/reference/airiam-ai-experts) |
| [List Models](actions/list-models.md) | `GET /api/v1/models` | [docs](https://docs.ai.airiam.com/reference/models) |
| [List Models With Body](actions/list-models-post.md) | `POST /api/v1/models/list` | [docs](https://docs.ai.airiam.com/reference/models) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/v1/workspaces` | [docs](https://docs.ai.airiam.com/reference/workspaces) |
| [Remove Model From Team](actions/remove-model-from-team.md) | `POST /api/v1/models/remove-from-team` | [docs](https://docs.ai.airiam.com/reference/models) |
| [Update Model](actions/update-model.md) | `PATCH /api/v1/models/:modelId` | [docs](https://docs.ai.airiam.com/reference/models) |
| [Update Workspace](actions/update-workspace.md) | `POST /api/v1/workspaces/:workspaceId` | [docs](https://docs.ai.airiam.com/reference/workspaces) |
| [Update Workspace Model](actions/update-workspace-model.md) | `POST /api/v1/workspaces/:workspaceId/:modelId` | [docs](https://docs.ai.airiam.com/reference/workspaces) |
