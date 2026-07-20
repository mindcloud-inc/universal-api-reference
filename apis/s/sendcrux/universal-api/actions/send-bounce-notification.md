# Sendcrux: Send Bounce Notification

Creates a bounce notification event in Sendcrux.

```
POST https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/send-bounce-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/send-bounce-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bounce_type": "hard",
  "message_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/send-bounce-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bounce_type": "hard",
    "message_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bounce_type` | string | yes | The bounce subtype to report, such as hard. Default: `hard`. |
| `description` | string | no | A human-readable explanation for the bounce event. |
| `message_id` | string | yes | The provider message identifier associated with the bounce event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "message": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `message` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Sendcrux API, this operation is `POST /api/v1/notification` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bounce-notification.md) for the provider-specific parameters and requirements.

