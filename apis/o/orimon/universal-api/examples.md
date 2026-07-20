# Orimon Universal API Examples

These examples use the MindCloud API key and Orimon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Message

Creates a chatbot message in Orimon.

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

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orimon/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "info.tenantId": "8c3a16ee-e978-4013-8209-9bea26d0c3e4",
    "info.psid": "visitor-123_tenant-abc",
    "message.payload.text": "What is Orimon?",
    "message.id": "msg-001"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "deliveredMsgId": "string",
        "messages": [
          {
            "chatLogId": "string",
            "deliveredMsgId": "string",
            "id": "string",
            "isTrainingRequired": true,
            "payload": {
              "relayData": {},
              "text": "string"
            },
            "psid": "string",
            "sender": "string",
            "sessionId": "string",
            "tenantId": "string",
            "timestamp": "2026-05-07T12:00:00.000Z",
            "type": "string"
          }
        ],
        "psid": "string",
        "rawMessage": "string",
        "sessionId": "string",
        "statuses": [
          {}
        ],
        "timestamp": "2026-05-07T12:00:00.000Z",
        "type": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Message action reference](actions/send-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orimon/latest/actions/send-message).
