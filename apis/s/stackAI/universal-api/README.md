# <img src="https://images.mindcloud.co/apps/icons/stack-ai_1775223348232.png" alt="Stack AI logo" width="28" height="28"> Stack AI: Universal API

Build, manage, and inspect Stack AI folders, connections, tools, and related runtime resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stackAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.stackai.com
- **Vendor API docs:** https://docs.stackai.com/api-reference/manager

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Personal Folder](actions/get-user-personal-folder.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-user-personal-folder?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Custom Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Tool](actions/create-custom-tool.md) | POST |  |
| [Delete Custom Tool](actions/delete-custom-tool.md) | DELETE |  |
| [List Custom Tools](actions/list-custom-tools.md) | GET |  |
| [Update Custom Tool](actions/update-custom-tool.md) | PUT |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [Get User Personal Folder](actions/get-user-personal-folder.md) | GET |  |
| [Query Folders](actions/query-folders.md) | GET |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST |  |
| [Get Knowledge Base by ID](actions/get-knowledge-base-by-id.md) | GET |  |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET |  |
| [Synchronize Knowledge Base](actions/synchronize-knowledge-base.md) | PUT |  |
| [Update Knowledge Base](actions/update-knowledge-base.md) | PUT |  |

### Knowledge Base Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST |  |
| [Get Resource by ID](actions/get-resource-by-id.md) | GET |  |
| [List Resources](actions/list-resources.md) | GET |  |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [Get StackAI Provider](actions/get-stackai-provider.md) | GET |  |
| [List StackAI Providers](actions/list-stackai-providers.md) | GET |  |

### Provider Action

| Action | Method | Description |
| --- | --- | --- |
| [Get Action by Provider and ID](actions/get-action-by-provider-and-id.md) | GET |  |

### Provider Action Input

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Inputs](actions/get-action-inputs.md) | GET |  |

### Provider Action Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Options](actions/get-action-options.md) | GET |  |

### Provider Action Output

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Outputs](actions/get-action-outputs.md) | GET |  |

### Provider Action Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Action](actions/run-action.md) | POST |  |

### Provider Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Get Trigger by Provider and ID](actions/get-trigger-by-provider-and-id.md) | GET |  |

### Stackai Action

| Action | Method | Description |
| --- | --- | --- |
| [List StackAI Actions](actions/list-stackai-actions.md) | GET |  |

### Stackai Tool

| Action | Method | Description |
| --- | --- | --- |
| [List StackAI Tools](actions/list-stackai-tools.md) | GET |  |

### Stackai Trigger

| Action | Method | Description |
| --- | --- | --- |
| [List StackAI Triggers](actions/list-stackai-triggers.md) | GET |  |

### Storage Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Storage Usage](actions/get-storage-usage.md) | GET |  |

