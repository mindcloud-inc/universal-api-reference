# <img src="https://images.mindcloud.co/apps/icons/cursor_1776800593308.png" alt="Cursor logo" width="28" height="28"> Cursor: Universal API

Create and manage Cursor Cloud Agents that work asynchronously on GitHub repositories, including agent launch, status, conversation, artifacts, models, repositories, and API key metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cursor/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cursor.com
- **Vendor API docs:** https://cursor.com/docs/cloud-agent/api/endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [API Key Info](actions/api-key-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [API Key Info](actions/api-key-info.md) | GET |  |

### Artifact

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Artifacts](actions/list-agent-artifacts.md) | GET |  |

### Artifact Download Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Artifact Download URL](actions/get-agent-artifact-download-url.md) | GET |  |

### Cloud Agent

| Action | Method | Description |
| --- | --- | --- |
| [Delete Agent](actions/delete-agent.md) | DELETE |  |
| [Get Agent Status](actions/get-agent-status.md) | GET |  |
| [Launch Agent](actions/launch-agent.md) | POST |  |
| [List Agents](actions/list-agents.md) | GET |  |
| [Stop Agent](actions/stop-agent.md) | PUT |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Conversation](actions/get-agent-conversation.md) | GET |  |

### Follow-up

| Action | Method | Description |
| --- | --- | --- |
| [Add Followup](actions/add-followup.md) | POST |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET |  |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [List GitHub Repositories](actions/list-github-repositories.md) | GET |  |

