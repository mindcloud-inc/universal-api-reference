# <img src="https://images.mindcloud.co/apps/icons/orimon_1775495869121.png" alt="Orimon logo" width="28" height="28"> Orimon: Universal API

Sales-focused generative AI chatbot platform for customer conversations and lead engagement.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orimon/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://orimon.ai
- **Vendor API docs:** https://orimon.gitbook.io/docs/developer-api/getting-started-with-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Message](actions/send-message.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orimon/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "info.tenantId": "8c3a16ee-e978-4013-8209-9bea26d0c3e4",
  "info.psid": "visitor-123_tenant-abc",
  "message.payload.text": "What is Orimon?",
  "message.id": "msg-001"
}'
```

## Actions (1)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Creates a chatbot message in Orimon. |

