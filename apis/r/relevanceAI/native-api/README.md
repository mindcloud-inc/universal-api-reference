# Relevance AI: Native API Reference

A consolidated summary of Relevance AI's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://sdk.relevanceai.com/get_started/10_1/quickstart
- **API base URL:** `https://api-{region}.stack.tryrelevance.com/latest`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Region:** `region` · required · Your Relevance AI project region code. Supported values are bcbe5a (US), d7b62b (EU), or f1db6c (AU).
- **Project:** `project` · required · Your Relevance AI project identifier from the Relevance AI dashboard.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/RelevanceAI/relevance-js-sdk/blob/main/docs/01_AUTH.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tool to Agent](actions/add-tool-to-agent.md) | `POST /agents/upsert` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Approve Task](actions/approve-task.md) | `POST /agents/trigger` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Clone Tool](actions/clone-tool.md) | `POST /studios/clone` | [docs](https://sdk.relevanceai.com/concepts/10_1/tools) |
| [Create Tool](actions/create-tool.md) | `POST /studios/bulk_update` | [docs](https://sdk.relevanceai.com/concepts/10_1/tools) |
| [Delete Agent](actions/delete-agent.md) | `POST /agents/:agentId/delete` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Delete Task](actions/delete-task.md) | `POST /knowledge/sets/delete` | [docs](https://sdk.relevanceai.com/concepts/10_1/knowledge) |
| [Delete Tool](actions/delete-tool.md) | `POST /studios/bulk_delete` | [docs](https://sdk.relevanceai.com/concepts/10_1/tools) |
| [Get Agent](actions/get-agent.md) | `GET /agents/:agentId/get` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Get Agent Trigger Message](actions/get-agent-trigger-message.md) | `GET /agents/:agentId/tasks/:conversationId/trigger_message` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Retrieve Knowledge Set Rows](actions/get-knowledge-rows.md) | `POST /knowledge/list` | [docs](https://sdk.relevanceai.com/concepts/10_1/knowledge) |
| [Get Task Metadata](actions/get-task-metadata.md) | `GET /knowledge/sets/:conversationId/get_metadata` | [docs](https://sdk.relevanceai.com/concepts/10_1/tasks) |
| [Get Task Output Preview](actions/get-task-output-preview.md) | `GET /agents/conversations/studios/list` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Get Tool](actions/get-tool.md) | `GET /studios/:toolId/get` | [docs](https://sdk.relevanceai.com/concepts/10_1/tools) |
| [Get Workforce](actions/get-workforce.md) | `GET /workforce/items/:workforceId` | [docs](https://relevanceai.com/docs/get-started/core-concepts/workforces) |
| [Get Workforce Task Messages](actions/get-workforce-task-messages.md) | `POST /workforce/items/:workforceId/tasks/:taskId/messages` | [docs](https://relevanceai.com/docs/build/workforces/workforce-features/workforce-task-view) |
| [Get Workforce Task Metadata](actions/get-workforce-task-metadata.md) | `GET /workforce/tasks/:taskId/metadata` | [docs](https://relevanceai.com/docs/build/workforces/workforce-features/workforce-task-view) |
| [List Agent Tasks](actions/list-agent-tasks.md) | `GET /agents/conversations/list` | [docs](https://sdk.relevanceai.com/concepts/tasks) |
| [List Agent Tools](actions/list-agent-tools.md) | `POST /agents/tools/list` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [List Agents](actions/list-agents.md) | `POST /agents/list` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [List Knowledge Sets](actions/list-knowledge-sets.md) | `POST /knowledge/sets/list` | [docs](https://sdk.relevanceai.com/concepts/10_1/knowledge) |
| [List Tools](actions/list-tools.md) | `GET /studios/list` | [docs](https://sdk.relevanceai.com/concepts/10_1/tools) |
| [List Workforce Tasks](actions/list-workforce-tasks.md) | `POST /workforce/tasks/list` | [docs](https://relevanceai.com/docs/build/workforces/workforce-features/workforce-task-view) |
| [Remove Tool from Agent](actions/remove-tool-from-agent.md) | `POST /agents/upsert` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Rerun Task](actions/rerun-task.md) | `POST /agents/trigger` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Schedule Action In Task](actions/schedule-agent-action.md) | `POST /agents/:agentId/scheduled_triggers_item/create` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Trigger Agent Task](actions/trigger-agent-task.md) | `POST /agents/trigger` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [Trigger Tool](actions/trigger-tool.md) | `POST /studios/:toolId/trigger_limited` | [docs](https://sdk.relevanceai.com/concepts/10_1/tools) |
| [Trigger Workforce Task](actions/trigger-workforce-task.md) | `POST /workforce/trigger` | [docs](https://relevanceai.com/docs/build/workforces/workforce-features/workforce-task-view) |
| [Upsert Agent](actions/upsert-agent.md) | `POST /agents/upsert` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
| [View Task Steps](actions/view-agent-task-steps.md) | `POST /agents/:agentId/tasks/:conversationId/view` | [docs](https://sdk.relevanceai.com/concepts/10_1/agents) |
