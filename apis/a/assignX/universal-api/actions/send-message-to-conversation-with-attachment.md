# AssignX: Send Message to Conversation with Attachment

Sends a message with an attachment in AssignX.

```
POST https://connect.mindcloud.co/v1/universal/assignX/latest/actions/send-message-to-conversation-with-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/send-message-to-conversation-with-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assignX/latest/actions/send-message-to-conversation-with-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Conversation identifier. |
| `message` | string | no | Optional message text to send with the attachment. |
| `file` | file | yes | Attachment file to upload to the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionObject": {},
      "agent": "string",
      "conversationId": "string",
      "messageId": "string",
      "response": "string",
      "status": 1,
      "trace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionObject` | object |  |
| `agent` | string |  |
| `conversationId` | string |  |
| `messageId` | string |  |
| `response` | string |  |
| `status` | number |  |
| `trace` | string |  |

## Native endpoint

Through the native AssignX API, this operation is `POST conversations/:id/attachment` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-conversation-with-attachment.md) for the provider-specific parameters and requirements.

