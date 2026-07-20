# <img src="https://images.mindcloud.co/apps/icons/custom-gptai_1774557694813.png" alt="CustomGPT.ai logo" width="28" height="28"> CustomGPT.ai: Universal API

Create, manage, and analyze AI agents, sources, and conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/customGPTai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://customgpt.ai/
- **Vendor API docs:** https://docs.customgpt.ai/reference/customgptai-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Profile](actions/get-current-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from a CustomGPT.ai agent. |
| [Get Document Metadata](actions/get-document-metadata.md) | GET | Retrieves document metadata from a CustomGPT.ai agent. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from a CustomGPT.ai agent. |
| [Reindex Document](actions/reindex-document.md) | PUT | Reindexes a URL-based document in a CustomGPT.ai agent. |
| [Update Document Metadata](actions/update-document-metadata.md) | PUT | Updates document metadata in a CustomGPT.ai agent. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in CustomGPT.ai. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from CustomGPT.ai. |
| [Get Agent Details](actions/get-agent-details.md) | GET | Retrieves detailed agent information from CustomGPT.ai. |
| [Get Agent Settings](actions/get-agent-settings.md) | GET | Retrieves current agent settings from CustomGPT.ai. |
| [Get Agent Statistics](actions/get-agent-statistics.md) | GET | Retrieves detailed agent statistics from CustomGPT.ai. |
| [List Agents](actions/list-agents.md) | GET | Retrieves all agents from your CustomGPT.ai account. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in CustomGPT.ai. |
| [Update Agent Settings](actions/update-agent-settings.md) | PUT | Updates current agent settings in CustomGPT.ai. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in a CustomGPT.ai agent. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from a CustomGPT.ai agent. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Source](actions/add-source.md) | POST | Adds a new source to a CustomGPT.ai agent. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from a CustomGPT.ai agent. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET | Retrieves the current user profile from CustomGPT.ai. |

