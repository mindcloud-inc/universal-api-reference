# Pachca: Create chat



```
POST https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat": {},
  "chat.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachca/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat": {},
    "chat.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chat` | object | yes | Chat parameters object. |
| `chat.name` | string | yes | Chat name. |
| `chat.member_ids[]` | array<number> | no | User IDs who will become chat members. Accepts multiple values as an array. |
| `chat.group_tag_ids[]` | array<number> | no | Group tag IDs to add as members. Accepts multiple values as an array. |
| `chat.channel` | boolean | no | Whether this chat is a channel. |
| `chat.public` | boolean | no | Whether this chat is publicly accessible. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "private": true,
      "public": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | boolean |  |
| `created_at` | date |  |
| `id` | number |  |
| `name` | string |  |
| `private` | boolean |  |
| `public` | boolean |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Pachca API, this operation is `POST /chats` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

