# Chatwork: Update Chat



```
PUT https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Room ID Example: `12345`. |
| `name` | string | no | Chat name Example: `Website renewal project`. |
| `description` | string | no | Chat description |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `iconPreset` | list<string> | no | Chat icon type One of: `beer`, `business`, `check`, `document`, `event`, `group`, `heart`, `idea`, `magcup`, `meeting`, `music`, `project`, `security`, `sports`, `star`, `study`, `travel`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roomId` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `PUT /rooms/:room_id` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat.md) for the provider-specific parameters and requirements.

