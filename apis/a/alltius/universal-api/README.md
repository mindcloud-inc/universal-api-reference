# <img src="https://images.mindcloud.co/apps/icons/alltius_1775826974569.png" alt="Alltius logo" width="28" height="28"> Alltius: Universal API

Query assistants and review Alltius chat sessions and reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/alltius/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.alltius.ai
- **Vendor API docs:** https://app.alltius.ai/api/platform/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Connection](actions/verify-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Ask Assistant](actions/ask-assistant.md) | GET | Submits a user query to an Alltius assistant. |
| [Delete User Chat Sessions](actions/delete-user-chat-sessions.md) | DELETE | Deletes chat sessions for an Alltius user. |
| [Get Chat History](actions/get-chat-history.md) | GET | Retrieves chat history for an Alltius session. |
| [Get Chat Sessions By User](actions/get-chat-sessions-by-user.md) | GET | Retrieves chat sessions for an Alltius user. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Rate Response](actions/rate-response.md) | PUT | Updates feedback for an Alltius assistant response. |
| [Verify Connection](actions/verify-connection.md) | GET | Submits a test prompt to verify an Alltius connection. |

