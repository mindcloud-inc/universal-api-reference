# ChatBot: Get Chat

Retrieves chat details from ChatBot API.

```
GET https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-chat?connectionId=$CONNECTION_ID&chatId=69bae986561b5000074c3ab8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "69bae986561b5000074c3ab8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-chat?${params}`, {
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
| `chatId` | string | yes | The required ChatBot chat ID from the request path. Example: `69bae986561b5000074c3ab8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finished": true,
      "id": "string",
      "messages": [
        {}
      ],
      "source": "string",
      "storyId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `createdAt` | date |  |
| `finished` | boolean |  |
| `id` | string |  |
| `messages` | array<object> |  |
| `source` | string |  |
| `storyId` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native ChatBot API, this operation is `GET /v2/chats/:chatId` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

