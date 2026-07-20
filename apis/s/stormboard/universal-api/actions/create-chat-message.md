# Stormboard: Create Chat Message

Creates a chat message in Stormboard.

```
POST https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "stormId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "stormId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | Chat message text to post in the storm. |
| `stormId` | number | yes | Storm ID from the Stormboard share dialog or related storm record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {
        "created": "string",
        "isnew": true,
        "msg": "string",
        "storm": 1,
        "user": {
          "avatar": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object |  |
| `message.created` | string |  |
| `message.isnew` | boolean |  |
| `message.msg` | string |  |
| `message.storm` | number |  |
| `message.user` | object |  |
| `message.user.avatar` | string |  |
| `message.user.id` | number |  |
| `message.user.name` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `POST /chat/:storm_id` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-message.md) for the provider-specific parameters and requirements.

