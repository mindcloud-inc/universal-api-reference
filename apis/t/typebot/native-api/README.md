# Typebot: Native API Reference

A consolidated summary of Typebot's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.typebot.io/api-reference
- **OpenAPI specification:** https://docs.typebot.io/openapi/builder.json
- **API base URL:** `https://app.typebot.io/api`

## Authentication

### API Key

Authenticate with a Typebot API token using a bearer Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.typebot.io/api-reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /v1/folders` | [docs](https://docs.typebot.io/api-reference/folder/create) |
| [Create Typebot](actions/create-typebot.md) | `POST /v1/typebots` | [docs](https://docs.typebot.io/api-reference/typebot/create) |
| [Create Workspace](actions/create-workspace.md) | `POST /v1/workspaces` | [docs](https://docs.typebot.io/api-reference/workspace/create) |
| [Delete Typebot](actions/delete-typebot.md) | `DELETE /v1/typebots/:typebotId` | [docs](https://docs.typebot.io/api-reference/typebot/delete) |
| [Get Folder](actions/get-folder.md) | `GET /v1/folders/:folderId` | [docs](https://docs.typebot.io/api-reference/folder/get) |
| [Get Published Typebot](actions/get-published-typebot.md) | `GET /v1/typebots/:typebotId/publishedTypebot` | [docs](https://docs.typebot.io/api-reference/typebot/get-published-bot) |
| [Get Result](actions/get-result.md) | `GET /v1/typebots/:typebotId/results/:resultId` | [docs](https://docs.typebot.io/api-reference/results/get) |
| [Get Result Transcript](actions/get-result-transcript.md) | `GET /v1/typebots/:typebotId/results/:resultId/transcript` | [docs](https://docs.typebot.io/openapi/builder.json) |
| [Get Results Stats](actions/get-results-stats.md) | `GET /v1/typebots/:typebotId/analytics/stats` | [docs](https://docs.typebot.io/api-reference/analytics/get-stats) |
| [Get Typebot](actions/get-typebot.md) | `GET /v1/typebots/:typebotId` | [docs](https://docs.typebot.io/api-reference/typebot/get) |
| [Get Workspace](actions/get-workspace.md) | `GET /v1/workspaces/:workspaceId` | [docs](https://docs.typebot.io/api-reference/workspace/get) |
| [Import Typebot](actions/import-typebot.md) | `POST /v1/typebots/import` | [docs](https://docs.typebot.io/api-reference/typebot/import) |
| [List Folders](actions/list-folders.md) | `GET /v1/folders` | [docs](https://docs.typebot.io/api-reference/folder/list) |
| [List Result Logs](actions/list-result-logs.md) | `GET /v1/typebots/:typebotId/results/:resultId/logs` | [docs](https://docs.typebot.io/api-reference/results/list-logs) |
| [List Results](actions/list-results.md) | `GET /v1/typebots/:typebotId/results` | [docs](https://docs.typebot.io/api-reference/results/list) |
| [List Typebots](actions/list-typebots.md) | `GET /v1/typebots` | [docs](https://docs.typebot.io/api-reference/typebot/list) |
| [List Workspace Members](actions/list-workspace-members.md) | `GET /v1/workspaces/:workspaceId/members` | [docs](https://docs.typebot.io/api-reference/workspace/list-members) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://docs.typebot.io/api-reference/workspace/list) |
| [Publish Typebot](actions/publish-typebot.md) | `POST /v1/typebots/:typebotId/publish` | [docs](https://docs.typebot.io/api-reference/typebot/publish) |
| [Unpublish Typebot](actions/unpublish-typebot.md) | `POST /v1/typebots/:typebotId/unpublish` | [docs](https://docs.typebot.io/api-reference/typebot/unpublish) |
| [Update Folder](actions/update-folder.md) | `PATCH /v1/folders/:folderId` | [docs](https://docs.typebot.io/api-reference/folder/update) |
| [Update Typebot](actions/update-typebot.md) | `PATCH /v1/typebots/:typebotId` | [docs](https://docs.typebot.io/api-reference/typebot/update) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /v1/workspaces/:workspaceId` | [docs](https://docs.typebot.io/api-reference/workspace/update) |
