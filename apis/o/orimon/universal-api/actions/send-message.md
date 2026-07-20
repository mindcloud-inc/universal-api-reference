# Orimon: Send Message

Creates a chatbot message in Orimon.

```
POST https://connect.mindcloud.co/v1/universal/orimon/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orimon `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `info.tenantId` | string | yes | The unique ID of the chatbot you want to message. Default: `8c3a16ee-e978-4013-8209-9bea26d0c3e4`. Example: `8c3a16ee-e978-4013-8209-9bea26d0c3e4`. |
| `info.psid` | string | yes | A unique session identifier for the end user; docs recommend a random value plus '_' plus the tenantId. Default: `mindcloud_orimon_session_8c3a16ee-e978-4013-8209-9bea26d0c3e4`. Example: `visitor-123_tenant-abc`. |
| `message.payload.text` | string | yes | The user message to send to the chatbot. Default: `Hello from MindCloud`. Example: `What is Orimon?`. |
| `message.id` | string | yes | A unique identifier for this input message. Default: `mindcloud-test-message-001`. Example: `msg-001`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.deliveredMsgId` | string | Delivered message identifier. |
| `data.messages` | array<object> | Returned message records. |
| `data.messages[].chatLogId` | string | Chat log record identifier. |
| `data.messages[].deliveredMsgId` | string | Delivered message ID echoed by Orimon. |
| `data.messages[].id` | string | Returned message identifier. |
| `data.messages[].isTrainingRequired` | boolean | Whether additional training is required. |
| `data.messages[].payload.relayData` | object | Additional relay payload data. |
| `data.messages[].payload.text` | string | Bot reply text. |
| `data.messages[].psid` | string | Session ID provided in the request. |
| `data.messages[].sender` | string | Message sender. |
| `data.messages[].sessionId` | string | Session identifier for the message. |
| `data.messages[].tenantId` | string | Tenant ID for the chatbot. |
| `data.messages[].timestamp` | date | Timestamp for the returned message. |
| `data.messages[].type` | string | Returned message type. |
| `data.psid` | string | Session identifier echoed by Orimon. |
| `data.rawMessage` | string | Full bot reply text. |
| `data.sessionId` | string | Orimon session identifier. |
| `data.statuses` | array<object> | Returned delivery statuses. |
| `data.timestamp` | date | Timestamp for the provider response. |
| `data.type` | string | Returned message envelope type. |
| `message` | string | Provider status message. |
| `status` | string | Overall request status. |

## Native endpoint

Through the native Orimon API, this operation is `POST /orimon/v1/conversation/api/message` (base URL `https://channel-connector.orimon.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

