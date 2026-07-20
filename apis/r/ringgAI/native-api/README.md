# Ringg AI: Native API Reference

A consolidated summary of Ringg AI's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.ringg.ai/api-reference/quick-start/guide
- **OpenAPI specification:** https://docs.ringg.ai/api-reference/openapi.json
- **API base URL:** `https://prod-api.ringg.ai/ca/api/v0`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.ringg.ai/api-reference/quick-start/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /public/agent` | [docs](https://docs.ringg.ai/api-reference/endpoint/assistant/create-agent) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /external/kb` | [docs](https://docs.ringg.ai/api-reference/endpoint/kb/create-knowledge-base) |
| [Delete Assistant](actions/delete-assistant.md) | `DELETE /agent/:agent_id` |  |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /calling/contact/:list_id` | [docs](https://docs.ringg.ai/api-reference/endpoint/contact/delete-contact-list) |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | `DELETE /external/kb/:kb_id` | [docs](https://docs.ringg.ai/api-reference/endpoint/kb/delete-knowledge-base) |
| [Download Call History](actions/download-call-history.md) | `POST /calling/history/download` | [docs](https://docs.ringg.ai/api-reference/endpoint/history/download-call-history) |
| [Edit Assistant](actions/edit-assistant.md) | `PATCH /agent/v1` | [docs](https://docs.ringg.ai/api-reference/endpoint/assistant/edit-assistant) |
| [Edit Knowledge Base](actions/edit-knowledge-base.md) | `PATCH /external/kb` | [docs](https://docs.ringg.ai/api-reference/endpoint/kb/edit-knowledge-base) |
| [Get All Campaigns](actions/get-all-campaigns.md) | `GET /campaign/all` | [docs](https://docs.ringg.ai/api-reference/endpoint/campaign/get-all-campaigns) |
| [Get All Knowledge Bases](actions/get-all-knowledge-bases.md) | `GET /external/kb/all` | [docs](https://docs.ringg.ai/api-reference/endpoint/kb/get-all-knowledge-bases) |
| [Get All User Workspaces](actions/get-all-user-workspaces.md) | `GET /workspace/all` | [docs](https://docs.ringg.ai/api-reference/endpoint/workspace/get-all-user-workspaces) |
| [Get Assistant By ID](actions/get-assistant-by-id.md) | `GET /agent/:agent_id` | [docs](https://docs.ringg.ai/api-reference/endpoint/assistant/get-assistant-by-id) |
| [Get Assistant Voices](actions/get-assistant-voices.md) | `GET /agent/voices` | [docs](https://docs.ringg.ai/api-reference/endpoint/assistant/get-assistant-voices) |
| [Get Assistants](actions/get-assistants.md) | `GET /agent/all` | [docs](https://docs.ringg.ai/api-reference/endpoint/assistant/get-assistants) |
| [Get Call Details](actions/get-call-details.md) | `GET /calling/call-details` | [docs](https://docs.ringg.ai/api-reference/endpoint/history/get-call-details) |
| [Get Call History](actions/get-call-history.md) | `GET /calling/history` | [docs](https://docs.ringg.ai/api-reference/endpoint/history/get-call-history) |
| [Get Classification Analytics](actions/get-classification-analytics.md) | `GET /analytics/classification-analytics` | [docs](https://docs.ringg.ai/api-reference/endpoint/analytics/get-classification-analytics) |
| [Get Drill-Down Analytics](actions/get-drill-down-analytics.md) | `GET /analytics/drill-down-analytics` | [docs](https://docs.ringg.ai/api-reference/endpoint/analytics/get-drill-down-analytics) |
| [Get Duration Distribution](actions/get-duration-distribution.md) | `GET /analytics/duration-distribution` | [docs](https://docs.ringg.ai/api-reference/endpoint/analytics/get-duration-distribution) |
| [Get Knowledge Base by ID](actions/get-knowledge-base-by-id.md) | `GET /external/kb/:kb_id` | [docs](https://docs.ringg.ai/api-reference/endpoint/kb/get-knowledge-base-by-id) |
| [Get Number Analytics](actions/get-number-analytics.md) | `GET /analytics/number-analytics` | [docs](https://docs.ringg.ai/api-reference/endpoint/analytics/get-number-analytics) |
| [Get Platform Analytics](actions/get-platform-analytics.md) | `GET /analytics/platform-analytics` | [docs](https://docs.ringg.ai/api-reference/endpoint/analytics/get-platform-analytics) |
| [Get Workspace Info](actions/get-workspace-info.md) | `GET /workspace` | [docs](https://docs.ringg.ai/api-reference/endpoint/workspace/get-workspace-info) |
| [Get Workspace Numbers](actions/get-workspace-numbers.md) | `GET /workspace/numbers` | [docs](https://docs.ringg.ai/api-reference/endpoint/numbers/get-workspace-numbers) |
| [Initiate Individual Call](actions/initiate-individual-call.md) | `POST /calling/outbound/individual` | [docs](https://docs.ringg.ai/api-reference/endpoint/calling/initiate-individual-call) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /workspace/users` | [docs](https://docs.ringg.ai/api-reference/endpoint/workspace/list-workspace-users) |
| [Regenerate API Key](actions/regenerate-api-key.md) | `PATCH /workspace/api-key` | [docs](https://docs.ringg.ai/api-reference/endpoint/workspace/regenerate-api-key) |
| [Start Campaign](actions/start-campaign.md) | `POST /campaign/start` | [docs](https://docs.ringg.ai/api-reference/endpoint/campaign/start-campaign) |
| [Terminate Calls by Call IDs](actions/terminate-calls-by-call-ids.md) | `PATCH /campaign/terminate` | [docs](https://docs.ringg.ai/api-reference/terminate/call-ids) |
| [Update Agent](actions/update-agent.md) | `PATCH /public/agent/:agent_id` |  |
| [Upload Campaign Contact List](actions/upload-campaign-contact-list.md) | `POST /campaign/save` | [docs](https://docs.ringg.ai/api-reference/endpoint/campaign/upload-campaign-contact-list) |
