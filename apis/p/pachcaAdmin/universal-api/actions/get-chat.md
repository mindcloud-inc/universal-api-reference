# Pachca (Admin): Get Chat

Retrieves a chat from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-chat?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-chat?${params}`, {
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
| `id` | number | yes | The Pachca chat ID. |

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

Through the native Pachca (Admin) API, this operation is `GET /chats/:id` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

