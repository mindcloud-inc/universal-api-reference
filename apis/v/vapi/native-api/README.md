# Vapi: Native API Reference

A consolidated summary of Vapi's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.vapi.ai/api-reference
- **OpenAPI specification:** https://docs.vapi.ai/openapi.json?api=b1efe1d4-3912-4115-a4b3-644d2c970f77
- **API base URL:** `https://api.vapi.ai`

## Authentication

### Private API Key

Use a Vapi private API key for management API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.vapi.ai/chat/quickstart)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | `POST /assistant` | [docs](https://docs.vapi.ai/api-reference/assistants/create) |
| [Create Call](actions/create-call.md) | `POST /call` | [docs](https://docs.vapi.ai/api-reference/calls/create) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign` | [docs](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-create) |
| [Create Chat](actions/create-chat.md) | `POST /chat` | [docs](https://docs.vapi.ai/api-reference/chats/create) |
| [Create Chat Response](actions/create-chat-response.md) | `POST /chat/responses` | [docs](https://docs.vapi.ai/api-reference/chats/create-response) |
| [Create Session](actions/create-session.md) | `POST /session` | [docs](https://docs.vapi.ai/api-reference/sessions/create) |
| [Create Squad](actions/create-squad.md) | `POST /squad` | [docs](https://docs.vapi.ai/api-reference/squads/create) |
| [Create Tool](actions/create-tool.md) | `POST /tool` | [docs](https://docs.vapi.ai/api-reference/tools/create) |
| [Delete Assistant](actions/delete-assistant.md) | `DELETE /assistant/:id` | [docs](https://docs.vapi.ai/api-reference/assistants/delete) |
| [Delete Call](actions/delete-call.md) | `DELETE /call/:id` | [docs](https://docs.vapi.ai/api-reference/calls/delete) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaign/:id` | [docs](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-remove) |
| [Delete Chat](actions/delete-chat.md) | `DELETE /chat/:id` | [docs](https://docs.vapi.ai/api-reference/chats/delete) |
| [Delete File](actions/delete-file.md) | `DELETE /file/:id` | [docs](https://docs.vapi.ai/api-reference/files/delete) |
| [Delete Session](actions/delete-session.md) | `DELETE /session/:id` | [docs](https://docs.vapi.ai/api-reference/sessions/delete) |
| [Delete Squad](actions/delete-squad.md) | `DELETE /squad/:id` | [docs](https://docs.vapi.ai/api-reference/squads/delete) |
| [Delete Tool](actions/delete-tool.md) | `DELETE /tool/:id` | [docs](https://docs.vapi.ai/api-reference/tools/delete) |
| [Get Assistant](actions/get-assistant.md) | `GET /assistant/:id` | [docs](https://docs.vapi.ai/api-reference/assistants/get) |
| [Get Call](actions/get-call.md) | `GET /call/:id` | [docs](https://docs.vapi.ai/api-reference/calls/get) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:id` | [docs](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-find-one) |
| [Get Chat](actions/get-chat.md) | `GET /chat/:id` | [docs](https://docs.vapi.ai/api-reference/chats/get) |
| [Get File](actions/get-file.md) | `GET /file/:id` | [docs](https://docs.vapi.ai/api-reference/files/get) |
| [Get Session](actions/get-session.md) | `GET /session/:id` | [docs](https://docs.vapi.ai/api-reference/sessions/get) |
| [Get Squad](actions/get-squad.md) | `GET /squad/:id` | [docs](https://docs.vapi.ai/api-reference/squads/get) |
| [Get Tool](actions/get-tool.md) | `GET /tool/:id` | [docs](https://docs.vapi.ai/api-reference/tools/get) |
| [List Assistants](actions/list-assistants.md) | `GET /assistant` | [docs](https://docs.vapi.ai/api-reference/assistants/list) |
| [List Calls](actions/list-calls.md) | `GET /call` | [docs](https://docs.vapi.ai/api-reference/calls/list) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaign` | [docs](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-find-all) |
| [List Chats](actions/list-chats.md) | `GET /chat` | [docs](https://docs.vapi.ai/api-reference/chats/list) |
| [List Files](actions/list-files.md) | `GET /file` | [docs](https://docs.vapi.ai/api-reference/files/list) |
| [List Sessions](actions/list-sessions.md) | `GET /session` | [docs](https://docs.vapi.ai/api-reference/sessions/list) |
| [List Squads](actions/list-squads.md) | `GET /squad` | [docs](https://docs.vapi.ai/api-reference/squads/list) |
| [List Tools](actions/list-tools.md) | `GET /tool` | [docs](https://docs.vapi.ai/api-reference/tools/list) |
| [Update Assistant](actions/update-assistant.md) | `PATCH /assistant/:id` | [docs](https://docs.vapi.ai/api-reference/assistants/update) |
| [Update Call](actions/update-call.md) | `PATCH /call/:id` | [docs](https://docs.vapi.ai/api-reference/calls/update) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaign/:id` | [docs](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-update) |
| [Update File](actions/update-file.md) | `PATCH /file/:id` | [docs](https://docs.vapi.ai/api-reference/files/update) |
| [Update Session](actions/update-session.md) | `PATCH /session/:id` | [docs](https://docs.vapi.ai/api-reference/sessions/update) |
| [Update Squad](actions/update-squad.md) | `PATCH /squad/:id` | [docs](https://docs.vapi.ai/api-reference/squads/update) |
| [Update Tool](actions/update-tool.md) | `PATCH /tool/:id` | [docs](https://docs.vapi.ai/api-reference/tools/update) |
| [Upload File](actions/upload-file.md) | `POST /file` | [docs](https://docs.vapi.ai/api-reference/files/create) |
