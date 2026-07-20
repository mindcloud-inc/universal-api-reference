# <img src="https://images.mindcloud.co/apps/icons/chatnode_1775503733196.png" alt="Chatnode logo" width="28" height="28"> Chatnode: Universal API

Chatnode lets you build AI agents trained on your data and access them through a small public API for authentication, chat, lead retrieval, and conversation history.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatnode/latest
- **Category:** Communication / Team Messaging
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chatnode.ai
- **Vendor API docs:** https://www.chatnode.ai/docs/developer-guides/api/quick-start

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate Me](actions/authenticate-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/authenticate-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Get Leads](actions/get-leads.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat History](actions/get-chat-history.md) | GET |  |
| [Send Message](actions/send-message.md) | POST |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Me](actions/authenticate-me.md) | GET |  |

