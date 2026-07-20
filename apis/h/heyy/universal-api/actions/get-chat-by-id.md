# Heyy: Get Chat by ID

Retrieves a chat by ID from Heyy.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-chat-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-chat-by-id?connectionId=$CONNECTION_ID&channelId=string&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-chat-by-id?${params}`, {
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
| `channelId` | string | yes | The Heyy channel ID. |
| `chatId` | string | yes | The Heyy chat ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `GET /[:channelId]/chats/:chatId` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-by-id.md) for the provider-specific parameters and requirements.

