# <img src="https://images.mindcloud.co/apps/icons/vecteezy-openai-chatgpt-logo-icon-22227364_1775579706020.png" alt="GPT Chatbot logo" width="28" height="28"> GPT Chatbot: Universal API

Build, manage, and interact with GPT Chatbot bots, agents, sessions, messages, and data sources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gPTChatbot/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gptchatbot.it
- **Vendor API docs:** https://docs.gptchatbot.it/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Chatbots](actions/list-chatbots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-chatbots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates an agent for a chatbot in GPT Chatbot. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from GPT Chatbot. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents for a chatbot in GPT Chatbot. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in GPT Chatbot. |

### Chatbot

| Action | Method | Description |
| --- | --- | --- |
| [Create Chatbot](actions/create-chatbot.md) | POST | Creates a chatbot in GPT Chatbot. |
| [Delete Chatbot](actions/delete-chatbot.md) | DELETE | Deletes an existing chatbot from GPT Chatbot. |
| [Get Chatbot](actions/get-chatbot.md) | GET | Retrieves a chatbot from GPT Chatbot. |
| [List Chatbots](actions/list-chatbots.md) | GET | Retrieves the current user's chatbots from GPT Chatbot. |
| [Update Chatbot](actions/update-chatbot.md) | PUT | Updates an existing chatbot in GPT Chatbot. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create QA Source](actions/create-qa-source.md) | POST | Creates a QA source for a chatbot in GPT Chatbot. |
| [Create URL Source](actions/create-url-source.md) | POST | Creates a URL source for a chatbot in GPT Chatbot. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from GPT Chatbot. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources for a chatbot in GPT Chatbot. |
| [Retrain Sources](actions/retrain-sources.md) | PUT | Retrains multiple URL sources in GPT Chatbot. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing source in GPT Chatbot. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file as a source for a chatbot in GPT Chatbot. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a streaming message for a session in GPT Chatbot. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from GPT Chatbot. |
| [Get Session History](actions/get-session-history.md) | GET | Retrieves a session's plain-text chat history from GPT Chatbot. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages for a session in GPT Chatbot. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a session for a chatbot in GPT Chatbot. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from GPT Chatbot. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from GPT Chatbot. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions for a chatbot in GPT Chatbot. |

