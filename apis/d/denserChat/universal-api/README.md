# <img src="https://images.mindcloud.co/apps/icons/denser-chat_1775591438271.png" alt="DenserChat logo" width="28" height="28"> DenserChat: Universal API

Query DenserChat chatbots over REST from custom apps, internal tools, and automations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/denserChat/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://denser.ai
- **Vendor API docs:** https://docs.denser.ai/docs/api/quick-start/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Chatbot](actions/query-chatbot.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/denserChat/latest/actions/query-chatbot?connectionId=$CONNECTION_ID&question=What%20are%20the%20pricing%20options%20for%20denserbot%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Chatbot Response

| Action | Method | Description |
| --- | --- | --- |
| [Query Chatbot](actions/query-chatbot.md) | GET | Retrieves a chatbot answer from DenserChat. |

