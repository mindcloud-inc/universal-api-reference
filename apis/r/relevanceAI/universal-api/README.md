# <img src="https://images.mindcloud.co/apps/icons/relevance-ai_1773783738406.png" alt="Relevance AI logo" width="28" height="28"> Relevance AI: Universal API

Build, deploy, and manage AI agents, tools, tasks, knowledge, and workforces in Relevance AI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/relevanceAI/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://relevanceai.com
- **Vendor API docs:** https://sdk.relevanceai.com/get_started/10_1/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tools](actions/list-tools.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Add Tool to Agent](actions/add-tool-to-agent.md) | PUT |  |
| [Delete Agent](actions/delete-agent.md) | DELETE |  |
| [Get Agent](actions/get-agent.md) | GET |  |
| [List Agents](actions/list-agents.md) | GET |  |
| [Remove Tool from Agent](actions/remove-tool-from-agent.md) | PUT |  |
| [Upsert Agent](actions/upsert-agent.md) | PUT |  |

### Knowledge Row

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Knowledge Set Rows](actions/get-knowledge-rows.md) | GET |  |

### Knowledge Set

| Action | Method | Description |
| --- | --- | --- |
| [List Knowledge Sets](actions/list-knowledge-sets.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Trigger Message](actions/get-agent-trigger-message.md) | GET |  |
| [Get Workforce Task Messages](actions/get-workforce-task-messages.md) | GET |  |
| [View Task Steps](actions/view-agent-task-steps.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Approve Task](actions/approve-task.md) | PUT |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task Metadata](actions/get-task-metadata.md) | GET |  |
| [Get Task Output Preview](actions/get-task-output-preview.md) | GET |  |
| [Get Workforce Task Metadata](actions/get-workforce-task-metadata.md) | GET |  |
| [List Agent Tasks](actions/list-agent-tasks.md) | GET |  |
| [List Workforce Tasks](actions/list-workforce-tasks.md) | GET |  |
| [Rerun Task](actions/rerun-task.md) | PUT |  |
| [Schedule Action In Task](actions/schedule-agent-action.md) | POST |  |
| [Trigger Agent Task](actions/trigger-agent-task.md) | POST |  |
| [Trigger Workforce Task](actions/trigger-workforce-task.md) | POST |  |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Clone Tool](actions/clone-tool.md) | POST |  |
| [Create Tool](actions/create-tool.md) | POST |  |
| [Delete Tool](actions/delete-tool.md) | DELETE |  |
| [Get Tool](actions/get-tool.md) | GET |  |
| [List Agent Tools](actions/list-agent-tools.md) | GET |  |
| [List Tools](actions/list-tools.md) | GET |  |
| [Trigger Tool](actions/trigger-tool.md) | POST |  |

### Workforce

| Action | Method | Description |
| --- | --- | --- |
| [Get Workforce](actions/get-workforce.md) | GET |  |

