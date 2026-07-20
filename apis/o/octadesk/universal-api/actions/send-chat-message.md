# Octadesk: Send Chat Message

Creates a message in an Octadesk chat.

```
POST https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/send-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "MindCloud test message",
  "channel": "web",
  "chatId": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e",
  "id": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e",
  "type": "public"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/send-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "MindCloud test message",
    "channel": "web",
    "chatId": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e",
    "id": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e",
    "type": "public"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | Message content. Example: `MindCloud test message`. |
| `channel` | string | yes | Channel that this message is from. Example: `web`. |
| `chatId` | string | yes | ID of the chat that this message will be included. Example: `07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e`. |
| `id` | string | yes | Chat ID from Octadesk. Example: `07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e`. |
| `type` | string | yes | Whether the message is intended for public or internal communication. Example: `public`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "chatId": "string",
      "id": "string",
      "readAt": "2026-05-07T12:00:00.000Z",
      "sentBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "status": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `chatId` | string |  |
| `id` | string |  |
| `readAt` | date |  |
| `sentBy.email` | string |  |
| `sentBy.id` | string |  |
| `sentBy.name` | string |  |
| `sentBy.type` | string |  |
| `status` | string |  |
| `time` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Octadesk API, this operation is `POST /chat/:id/messages` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.

