# HelpCrunch: List Chat Messages

Retrieves messages from a chat in HelpCrunch.

```
GET https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-chat-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "chatId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-chat-messages?${params}`, {
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
| `chatId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "broadcastType": "string",
      "chat": 1,
      "createdAt": "string",
      "edited": true,
      "from": "string",
      "id": 1,
      "read": true,
      "text": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `broadcastType` | string |  |
| `chat` | number |  |
| `createdAt` | string |  |
| `edited` | boolean |  |
| `from` | string |  |
| `id` | number |  |
| `read` | boolean |  |
| `text` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native HelpCrunch API, this operation is `GET /chats/:chatId/messages` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chat-messages.md) for the provider-specific parameters and requirements.

