# <img src="https://images.mindcloud.co/apps/icons/d-onnajameseasy_1775853054403.png" alt="DONNAJAMES Easy logo" width="28" height="28"> DONNAJAMES Easy: Universal API

AI chatbot, agent, session, message, data-source, and source-tag operations for the GPT-Trainer-backed DONNAJAMES Easy workspace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dONNAJAMESEasy/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.gpt-trainer.com
- **Vendor API docs:** https://guide.gpt-trainer.com/api-reference/api-key-setup

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch All Chatbots](actions/fetch-all-chatbots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-chatbots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent for a chatbot in DONNAJAMES Easy. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from DONNAJAMES Easy. |
| [Fetch All Agents](actions/fetch-all-agents.md) | GET | Retrieves all agents for a chatbot from DONNAJAMES Easy. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in DONNAJAMES Easy. |

### Chatbot

| Action | Method | Description |
| --- | --- | --- |
| [Create Chatbot](actions/create-chatbot.md) | POST | Creates a new chatbot in DONNAJAMES Easy. |
| [Delete Chatbot](actions/delete-chatbot.md) | DELETE | Deletes an existing chatbot from DONNAJAMES Easy. |
| [Fetch a Chatbot](actions/fetch-a-chatbot.md) | GET | Retrieves a chatbot from DONNAJAMES Easy. |
| [Fetch All Chatbots](actions/fetch-all-chatbots.md) | GET | Retrieves all chatbots from DONNAJAMES Easy. |
| [Update Chatbot](actions/update-chatbot.md) | PUT | Updates an existing chatbot in DONNAJAMES Easy. |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Create QA Source](actions/create-qa-source.md) | POST | Creates a new QA source in DONNAJAMES Easy. |
| [Create URL Source](actions/create-url-source.md) | POST | Creates a new URL source in DONNAJAMES Easy. |
| [Delete Multiple Sources](actions/delete-multiple-sources.md) | DELETE | Deletes multiple sources from DONNAJAMES Easy. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from DONNAJAMES Easy. |
| [Fetch List of Sources](actions/fetch-list-of-sources.md) | GET | Retrieves all sources for a chatbot from DONNAJAMES Easy. |
| [Retrain Sources](actions/retrain-sources.md) | PUT | Retrains URL sources in DONNAJAMES Easy. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing source in DONNAJAMES Easy. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new session message in DONNAJAMES Easy. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from DONNAJAMES Easy. |
| [Delete Multiple Messages](actions/delete-multiple-messages.md) | DELETE | Deletes multiple messages from DONNAJAMES Easy. |
| [Fetch All Messages](actions/fetch-all-messages.md) | GET | Retrieves all messages for a session from DONNAJAMES Easy. |
| [Fetch Session History](actions/fetch-session-history.md) | GET | Retrieves a session transcript from DONNAJAMES Easy. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new session for a chatbot in DONNAJAMES Easy. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from DONNAJAMES Easy. |
| [Fetch a Session](actions/fetch-a-session.md) | GET | Retrieves a chatbot session from DONNAJAMES Easy. |
| [Fetch All Sessions](actions/fetch-all-sessions.md) | GET | Retrieves all sessions for a chatbot from DONNAJAMES Easy. |

### Source Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Source Tag](actions/create-source-tag.md) | POST | Creates a new source tag in DONNAJAMES Easy. |
| [Delete Source Tag](actions/delete-source-tag.md) | DELETE | Deletes an existing source tag from DONNAJAMES Easy. |
| [Fetch All Source Tags](actions/fetch-all-source-tags.md) | GET | Retrieves all source tags from DONNAJAMES Easy. |
| [Update Source Tag](actions/update-source-tag.md) | PUT | Updates an existing source tag in DONNAJAMES Easy. |

