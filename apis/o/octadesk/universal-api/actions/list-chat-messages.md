# Octadesk: List Chat Messages

Retrieves messages from an Octadesk chat.

```
GET https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&id=07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chat-messages?${params}`, {
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
| `id` | string | yes | Chat ID from Octadesk. Example: `07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e`. |

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

Through the native Octadesk API, this operation is `GET /chat/:id/messages` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

