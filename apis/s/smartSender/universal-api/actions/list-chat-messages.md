# Smart Sender: List Chat Messages

Retrieves messages for a chat in Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-chat-messages?${params}`, {
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
| `activities` | boolean | no | Whether to include system messages in the results. |
| `chatId` | string | yes | The Smart Sender chat ID. |

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

Through the native Smart Sender API, this operation is `GET /v1/chats/:chatId/messages` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

