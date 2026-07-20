# <img src="https://images.mindcloud.co/apps/icons/images-28_1776983920879.png" alt="SectorFlow.AI logo" width="28" height="28"> SectorFlow.AI: Universal API

SectorFlow.AI provides an AI platform for accessing and using large language models, workspaces, chat completions, and expert/document workflows through its hosted platform API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sectorFlowAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sectorflow.ai
- **Vendor API docs:** https://docs.sectorflow.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Prompt Logs CSV](actions/get-prompt-logs-csv.md) | GET |  |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST |  |

### Chat History

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat History](actions/get-chat-history.md) | GET |  |

### Chat Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat Thread](actions/get-chat-thread.md) | GET |  |
| [Update Chat Thread Title](actions/update-chat-thread-title.md) | PUT |  |

### Expert

| Action | Method | Description |
| --- | --- | --- |
| [Get Expert](actions/get-expert.md) | GET |  |
| [List Experts](actions/list-experts.md) | GET |  |

### Expert File Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Expert File Content](actions/get-expert-file-content.md) | GET |  |

### Expert Prompt Context

| Action | Method | Description |
| --- | --- | --- |
| [Get Expert Context For Prompt](actions/get-expert-context-for-prompt.md) | GET |  |

### Greeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Greeting](actions/get-greeting.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion Stream](actions/create-chat-completion-stream.md) | POST |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Models From List](actions/get-active-models-from-list.md) | GET |  |
| [Get All Active Models From List](actions/get-all-active-models-from-list.md) | GET |  |
| [Get Model](actions/get-model.md) | GET |  |
| [List All Models](actions/list-all-models.md) | GET |  |
| [List Models](actions/list-models.md) | GET |  |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Add Model To Team](actions/add-model-to-team.md) | PUT |  |
| [Create Model](actions/create-model.md) | POST |  |
| [Remove Model From Team](actions/remove-model-from-team.md) | PUT |  |
| [Update Model](actions/update-model.md) | PUT |  |

### Prompt Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Paged Prompt Logs](actions/get-paged-prompt-logs.md) | GET |  |
| [Search Prompt Logs](actions/search-prompt-logs.md) | GET |  |

### Sample Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Get Sample Prompts](actions/get-sample-prompts.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

