# Pachca (Admin): Create Chat

Creates a new chat in the Pachca Admin API.

```
POST https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chat.name` | string | yes |  |
| `chat.memberIds[]` | array<number> | no |  |
| `chat.groupTagIds[]` | array<number> | no |  |
| `chat.channel` | boolean | no |  |
| `chat.public` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "channel": true,
        "createdAt": "string",
        "id": 1,
        "lastMessageAt": "string",
        "meetRoomUrl": "https://example.com",
        "memberIds": [
          1
        ],
        "name": "Ava Chen",
        "ownerId": 1,
        "personal": true,
        "public": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.channel` | boolean |  |
| `data.createdAt` | string |  |
| `data.id` | number |  |
| `data.lastMessageAt` | string |  |
| `data.meetRoomUrl` | string |  |
| `data.memberIds[]` | number |  |
| `data.name` | string |  |
| `data.ownerId` | number |  |
| `data.personal` | boolean |  |
| `data.public` | boolean |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `POST /chats` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

