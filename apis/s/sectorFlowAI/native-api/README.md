# SectorFlow.AI: Native API Reference

A consolidated summary of SectorFlow.AI's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.sectorflow.ai/
- **API base URL:** `https://platform.sectorflow.ai/api/v1`

## Authentication

### API Key

Authenticate to SectorFlow with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.sectorflowai.com/reference/getting-started-with-your-api-1)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Model To Team](actions/add-model-to-team.md) | `POST /models/add-to-team` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /chat/{workspaceId}/completions` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Create Chat Completion Stream](actions/create-chat-completion-stream.md) | `POST /chat/{workspaceId}/completions/stream` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Create Model](actions/create-model.md) | `POST /models` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://docs.sectorflowai.com/reference/getting-started-with-your-api-1) |
| [Get Active Models From List](actions/get-active-models-from-list.md) | `POST /models/list` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Get All Active Models From List](actions/get-all-active-models-from-list.md) | `POST /models/list/all` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Get Chat History](actions/get-chat-history.md) | `GET /chat/{workspaceId}/history` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Get Chat Thread](actions/get-chat-thread.md) | `GET /chat/{workspaceId}/history/{threadId}` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Get Expert](actions/get-expert.md) | `GET /plus/{plusId}` | [docs](https://docs.sectorflowai.com/reference/sectorplus-1) |
| [Get Expert Context For Prompt](actions/get-expert-context-for-prompt.md) | `POST /plus/{plusId}/context-for-prompt` | [docs](https://docs.sectorflowai.com/reference/sectorplus-1) |
| [Get Expert File Content](actions/get-expert-file-content.md) | `GET /plus/file/{fileId}/content` | [docs](https://docs.sectorflowai.com/reference/sectorplus-1) |
| [Get Greeting](actions/get-greeting.md) | `GET /chat/{workspaceId}/greeting` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Get Model](actions/get-model.md) | `GET /models/{modelId}` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Get Paged Prompt Logs](actions/get-paged-prompt-logs.md) | `GET /chat/prompt-logs/paged` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Get Prompt Logs CSV](actions/get-prompt-logs-csv.md) | `GET /chat/prompt-logs/csv` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Get Sample Prompts](actions/get-sample-prompts.md) | `GET /chat/{workspaceId}/sample-prompts` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [List All Models](actions/list-all-models.md) | `GET /models/all` | [docs](https://docs.sectorflowai.com/reference/models) |
| [List Experts](actions/list-experts.md) | `GET /plus` | [docs](https://docs.sectorflowai.com/reference/sectorplus-1) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://docs.sectorflowai.com/reference/models) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://docs.sectorflowai.com/reference/getting-started-with-your-api-1) |
| [Remove Model From Team](actions/remove-model-from-team.md) | `POST /models/remove-from-team` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Search Prompt Logs](actions/search-prompt-logs.md) | `GET /chat/prompt-logs` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Update Chat Thread Title](actions/update-chat-thread-title.md) | `POST /chat/{workspaceId}/history/{threadId}` | [docs](https://docs.sectorflowai.com/reference/chat) |
| [Update Model](actions/update-model.md) | `PATCH /models/{modelId}` | [docs](https://docs.sectorflowai.com/reference/models) |
| [Update Workspace](actions/update-workspace.md) | `POST /workspaces/{workspaceId}` | [docs](https://docs.sectorflowai.com/reference/getting-started-with-your-api-1) |
