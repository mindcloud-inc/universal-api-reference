# Pushbullet: Update Chat

Updates an existing chat in Pushbullet.

```
PUT https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chat_iden": "string",
  "muted": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chat_iden": "string",
    "muted": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chat_iden` | string | yes | Chat identifier to update. |
| `muted` | boolean | yes | Set true to mute the chat and false to unmute. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": 1,
      "email": "ava@example.com",
      "iden": "string",
      "modified": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | number |  |
| `email` | string |  |
| `iden` | string |  |
| `modified` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `POST /chats/:chat_iden` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat.md) for the provider-specific parameters and requirements.

