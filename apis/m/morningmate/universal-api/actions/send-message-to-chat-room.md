# Morningmate: Send Message to Chat Room

Creates a message in a Morningmate chat room.

```
POST https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/send-message-to-chat-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/send-message-to-chat-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "12345",
  "registerId": "apps@mindcloud.co",
  "contents": "Created by Codex during Morningmate verification."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/send-message-to-chat-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "12345",
    "registerId": "apps@mindcloud.co",
    "contents": "Created by Codex during Morningmate verification."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Morningmate numeric chat room ID Example: `12345`. |
| `registerId` | string | yes | Morningmate author user ID Example: `apps@mindcloud.co`. |
| `contents` | string | yes | Message body Example: `Created by Codex during Morningmate verification.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageId` | string |  |

## Native endpoint

Through the native Morningmate API, this operation is `POST /v1/chats/[:roomId]/messages` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-chat-room.md) for the provider-specific parameters and requirements.

