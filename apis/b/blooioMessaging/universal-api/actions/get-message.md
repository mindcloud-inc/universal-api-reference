# Blooio Messaging: Get Message

Retrieves a message from Blooio Messaging.

```
GET https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-message?connectionId=$CONNECTION_ID&chatId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-message?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | Chat identifier. Use a phone number, email, group ID, or comma-separated recipient list. |
| `messageId` | string | yes | Message identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_id": "string",
      "created_at": 1,
      "message_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_id` | string |  |
| `created_at` | number |  |
| `message_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `GET /chats/{chatId}/messages/{messageId}` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

