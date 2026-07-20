# Pushbullet: Create Chat

Creates a new chat in Pushbullet.

```
POST https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Recipient email for the chat. |
| `muted` | boolean | no | Set true to mute the chat after creation. |

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

Through the native Pushbullet API, this operation is `POST /chats` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

