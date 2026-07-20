# Morningmate: List Chat Rooms

Retrieves chat rooms for a Morningmate participant.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-chat-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-chat-rooms?connectionId=$CONNECTION_ID&participantId=apps%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "participantId": "apps@mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-chat-rooms?${params}`, {
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
| `participantId` | string | yes | Morningmate participant user ID Example: `apps@mindcloud.co`. |

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

Through the native Morningmate API, this operation is `GET /v1/chats/participants/[:participantId]` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-rooms.md) for the provider-specific parameters and requirements.

