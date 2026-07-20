# Heyy: Update Chat

Updates an existing chat in a Heyy channel.

```
PUT https://connect.mindcloud.co/v1/universal/heyy/latest/actions/update-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/update-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "chatId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/update-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "chatId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTeamId` | string | no | The assigned team ID. |
| `assignedUserId` | string | no | The assigned user ID. |
| `channelId` | string | yes | The channel ID. |
| `chatId` | string | yes | The chat ID. |
| `isUnread` | boolean | no | Whether the chat should be marked unread. |
| `status` | string | no | The chat status. |

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

Through the native Heyy API, this operation is `PUT /[:channelId]/chats/:chatId` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat.md) for the provider-specific parameters and requirements.

