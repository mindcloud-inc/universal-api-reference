# Habitica: Send Private Message

Sends a private message to a Habitica member.

```
POST https://connect.mindcloud.co/v1/universal/habitica/latest/actions/send-private-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/send-private-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toUserId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/habitica/latest/actions/send-private-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toUserId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toUserId` | string | yes | The Habitica member ID that should receive the private message. |
| `message` | string | yes | The message text to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appVersion": "string",
      "message": {},
      "notifications": [
        {}
      ],
      "userV": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appVersion` | string |  |
| `message` | object |  |
| `notifications` | array<object> |  |
| `userV` | number |  |

## Native endpoint

Through the native Habitica API, this operation is `POST /members/send-private-message` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-private-message.md) for the provider-specific parameters and requirements.

