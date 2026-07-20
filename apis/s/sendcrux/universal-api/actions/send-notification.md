# Sendcrux: Send Notification

Creates a notification event in Sendcrux.

```
POST https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message_id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message_id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bounce_type` | string | no | The bounce subtype when `type=bounced`. |
| `description` | string | no | A human-readable explanation for the notification event. |
| `message_id` | string | yes | The provider message identifier associated with the delivery event. |
| `report_type` | string | no | The report type when `type=abuse` or `type=spam`. |
| `type` | string | yes | The notification type, such as sent, bounced, abuse, spam, or failed. |

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

Through the native Sendcrux API, this operation is `POST /api/v1/notification` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

