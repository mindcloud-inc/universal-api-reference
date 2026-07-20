# Morningmate: Get Chat Room

Retrieves a chat room from Morningmate by room ID.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/get-chat-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/get-chat-room?connectionId=$CONNECTION_ID&roomId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/get-chat-room?${params}`, {
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
| `roomId` | number | yes | Morningmate numeric chat room ID Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "registerId": "string",
      "registerName": "Ava Chen",
      "roomId": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `registerId` | string | Register ID. |
| `registerName` | string | Register name. |
| `roomId` | string | Chat room ID. |
| `title` | string | Chat room title. |
| `type` | string | Chat room type. |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v1/chats/[:roomId]` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-room.md) for the provider-specific parameters and requirements.

