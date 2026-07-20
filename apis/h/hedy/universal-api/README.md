# <img src="https://images.mindcloud.co/apps/icons/hedy_1774032367171.png" alt="Hedy logo" width="28" height="28"> Hedy: Universal API

Access sessions, highlights, todos, topics, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hedy/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hedy.ai
- **Vendor API docs:** https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sessions](actions/list-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Highlight

| Action | Method | Description |
| --- | --- | --- |
| [Get Highlight Details](actions/get-highlight-details.md) | GET | Retrieves a highlight from Hedy. |
| [List Highlights](actions/list-highlights.md) | GET | Retrieves highlight records from Hedy. |
| [List Session Highlights](actions/list-session-highlights.md) | GET | Retrieves highlights for a Hedy session. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Details](actions/get-session-details.md) | GET | Retrieves a session from Hedy. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves session records from Hedy. |
| [List Topic Sessions](actions/list-topic-sessions.md) | GET | Retrieves sessions for a Hedy topic. |

### Session Context

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Context](actions/create-session-context.md) | POST | Creates a new session context in Hedy. |
| [Delete Session Context](actions/delete-session-context.md) | DELETE | Deletes a session context from Hedy. |
| [Get Session Context](actions/get-session-context.md) | GET | Retrieves a session context from Hedy. |
| [List Session Contexts](actions/list-session-contexts.md) | GET | Retrieves session context records from Hedy. |
| [Update Session Context](actions/update-session-context.md) | PUT | Updates an existing session context in Hedy. |

### To-do Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Session To-Do Item](actions/get-session-to-do-item.md) | GET | Retrieves a to-do item from a Hedy session. |
| [List Session To-Do Items](actions/list-session-to-do-items.md) | GET | Retrieves to-do items for a Hedy session. |
| [List To-Do Items](actions/list-to-do-items.md) | GET | Retrieves to-do items from Hedy. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Create Topic](actions/create-topic.md) | POST | Creates a new topic in Hedy. |
| [Delete Topic](actions/delete-topic.md) | DELETE | Deletes a topic from Hedy. |
| [Get Topic Details](actions/get-topic-details.md) | GET | Retrieves a topic from Hedy. |
| [List Topics](actions/list-topics.md) | GET | Retrieves topics from Hedy. |
| [Update Topic](actions/update-topic.md) | PUT | Updates an existing topic in Hedy. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Hedy. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Hedy. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Hedy. |

