# Sign.Plus: Set Envelope Notification



```
PUT https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/set-envelope-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/set-envelope-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelopeId": "string",
  "subject": "string",
  "message": "string",
  "reminderInterval": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/set-envelope-notification', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "envelopeId": "string",
    "subject": "string",
    "message": "string",
    "reminderInterval": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `envelopeId` | string | yes |  |
| `subject` | string | yes |  |
| `message` | string | yes |  |
| `reminderInterval` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {},
      "comment": "string",
      "created_at": 1,
      "documents": [
        {}
      ],
      "expires_at": 1,
      "flow_type": "string",
      "id": "string",
      "is_duplicable": true,
      "legality_level": "string",
      "name": "Ava Chen",
      "notification": {},
      "num_recipients": 1,
      "pages": 1,
      "signing_steps": [
        {}
      ],
      "status": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | object |  |
| `comment` | string |  |
| `created_at` | number |  |
| `documents` | array<object> |  |
| `expires_at` | number |  |
| `flow_type` | string |  |
| `id` | string |  |
| `is_duplicable` | boolean |  |
| `legality_level` | string |  |
| `name` | string |  |
| `notification` | object |  |
| `num_recipients` | number |  |
| `pages` | number |  |
| `signing_steps` | array<object> |  |
| `status` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Sign.Plus API, this operation is `PUT /envelope/:envelope_id/set_notification` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-envelope-notification.md) for the provider-specific parameters and requirements.

