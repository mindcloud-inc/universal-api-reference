# Chatwork: Mark Messages Read



```
PUT https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/mark-messages-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/mark-messages-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "123456789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/mark-messages-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "123456789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Room ID. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mentionNum": 1,
      "unreadNum": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mentionNum` | number |  |
| `unreadNum` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `PUT /rooms/:room_id/messages/read` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-messages-read.md) for the provider-specific parameters and requirements.

