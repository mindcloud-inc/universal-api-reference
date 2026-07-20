# Smart Sender: Send Message

Sends a message to a contact in Smart Sender.

```
POST https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "content": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "content": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The Smart Sender contact ID. |
| `content` | string | yes | Text content for text messages. |
| `type` | string | yes | The type of message to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deliveredAt": "2026-05-07T12:00:00.000Z",
      "editedAt": "2026-05-07T12:00:00.000Z",
      "gate": {},
      "id": 1,
      "internal": true,
      "seenAt": "2026-05-07T12:00:00.000Z",
      "sender": {},
      "state": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `createdAt` | date |  |
| `deliveredAt` | date |  |
| `editedAt` | date |  |
| `gate` | object |  |
| `id` | number |  |
| `internal` | boolean |  |
| `seenAt` | date |  |
| `sender` | object |  |
| `state` | object |  |

## Native endpoint

Through the native Smart Sender API, this operation is `POST /v1/contacts/:contactId/send` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

