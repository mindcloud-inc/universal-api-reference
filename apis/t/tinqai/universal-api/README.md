# <img src="https://images.mindcloud.co/apps/icons/tinqai_1775253930515.png" alt="Tinq.ai logo" width="28" height="28"> Tinq.ai: Universal API

Connect knowledge sources and power context-aware AI assistants

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tinqai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tinq.ai/
- **Vendor API docs:** https://docs.tinq.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace](actions/get-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET |  |

### Datasource

| Action | Method | Description |
| --- | --- | --- |
| [Get Datasource](actions/get-datasource.md) | GET |  |
| [List Datasources](actions/list-datasources.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Documents](actions/delete-documents.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Datasource Documents](actions/list-datasource-documents.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Sync Datasource Documents](actions/sync-datasource-documents.md) | PUT |  |

### Enhanced Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Enhance Prompt](actions/enhance-prompt.md) | POST |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET |  |

### Rewrite Result

| Action | Method | Description |
| --- | --- | --- |
| [Rewrite Text](actions/rewrite-text.md) | POST |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Workspace](actions/search-workspace.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Status](actions/get-task-status.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET |  |

