# <img src="https://images.mindcloud.co/apps/icons/chatsistant-icon_1775657991171.png" alt="Chatsistant logo" width="28" height="28"> Chatsistant: Universal API

Chatsistant lets teams build AI chatbots, agents, sessions, messages, data sources, and source tags through a bearer-token REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatsistant/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chatsistant.com
- **Vendor API docs:** https://docs.chatsistant.com/api-reference/api-key-setup

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Chatbots](actions/list-chatbots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-chatbots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Create Chatbot](actions/create-chatbot.md) | POST | Creates a new chatbot in Chatsistant. |
| [Delete Chatbot](actions/delete-chatbot.md) | DELETE | Deletes an existing chatbot from Chatsistant. |
| [Get Chatbot](actions/get-chatbot.md) | GET | Retrieves chatbot details from Chatsistant. |
| [List Chatbots](actions/list-chatbots.md) | GET | Retrieves chatbot records from Chatsistant. |
| [Update Chatbot](actions/update-chatbot.md) | PUT | Updates an existing chatbot in Chatsistant. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create QA Source](actions/create-qa-source.md) | POST | Creates a new QA source in Chatsistant. |
| [Create URL Source](actions/create-url-source.md) | POST | Creates a new URL source in Chatsistant. |
| [Delete Multiple Sources](actions/delete-multiple-sources.md) | DELETE | Deletes multiple sources from Chatsistant. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from Chatsistant. |
| [List Sources](actions/list-sources.md) | GET | Retrieves data source records from Chatsistant. |
| [Retrain Sources](actions/retrain-sources.md) | PUT | Retrains existing URL sources in Chatsistant. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing source in Chatsistant. |
| [Upload File Source](actions/upload-file-source.md) | POST | Creates a new file source in Chatsistant. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new session message in Chatsistant. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from Chatsistant. |
| [Delete Multiple Messages](actions/delete-multiple-messages.md) | DELETE | Deletes multiple messages from Chatsistant. |
| [List Messages](actions/list-messages.md) | GET | Retrieves session message records from Chatsistant. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new chatbot agent in Chatsistant. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing chatbot agent from Chatsistant. |
| [List Agents](actions/list-agents.md) | GET | Retrieves chatbot agent records from Chatsistant. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing chatbot agent in Chatsistant. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new chatbot session in Chatsistant. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing chatbot session from Chatsistant. |
| [Get Session](actions/get-session.md) | GET | Retrieves chatbot session details from Chatsistant. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves chatbot session records from Chatsistant. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Source Tag](actions/create-source-tag.md) | POST | Creates a new source tag in Chatsistant. |
| [Delete Source Tag](actions/delete-source-tag.md) | DELETE | Deletes an existing source tag from Chatsistant. |
| [List Source Tags](actions/list-source-tags.md) | GET | Retrieves source tag records from Chatsistant. |
| [Update Source Tag](actions/update-source-tag.md) | PUT | Updates an existing source tag in Chatsistant. |

