# <img src="https://images.mindcloud.co/apps/icons/dust_1773771323984.png" alt="Dust logo" width="28" height="28"> Dust: Universal API

Ask Dust agents and manage workspace knowledge

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dust/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dust.tt
- **Vendor API docs:** https://docs.dust.tt/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dust/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agents](actions/list-agents.md) | GET | Retrieves agent configurations from the Dust workspace. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Dust. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Dust by ID. |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Sources](actions/get-data-sources.md) | GET | Retrieves data sources from a Dust space. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Search Data Source](actions/search-data-source.md) | GET |  |
| [Upsert Document](actions/upsert-document.md) | POST |  |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves available spaces from the Dust workspace. |

