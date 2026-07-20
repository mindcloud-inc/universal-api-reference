# SuperSend: Retry Webhook Delivery

Retries a webhook delivery in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/retry-webhook-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/retry-webhook-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "deliveryId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/retry-webhook-delivery', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "deliveryId": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `deliveryId` | string | yes |  |
| `teamId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempt_count": 1,
      "campaign": {
        "id": "string",
        "name": "Ava Chen"
      },
      "contact": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "delivered_at": "2026-05-07T12:00:00.000Z",
      "error_message": "string",
      "event_id": "string",
      "event_type": "string",
      "id": "string",
      "last_attempt_at": "2026-05-07T12:00:00.000Z",
      "max_attempts": 1,
      "next_retry_at": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "payload": {},
      "response_status": 1,
      "response_time_ms": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempt_count` | number |  |
| `campaign.id` | string |  |
| `campaign.name` | string |  |
| `contact.email` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `created_at` | date |  |
| `delivered_at` | date |  |
| `error_message` | string |  |
| `event_id` | string |  |
| `event_type` | string |  |
| `id` | string |  |
| `last_attempt_at` | date |  |
| `max_attempts` | number |  |
| `next_retry_at` | date |  |
| `object` | string |  |
| `payload` | object |  |
| `response_status` | number |  |
| `response_time_ms` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /webhooks/{id}/deliveries/{deliveryId}/retry` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retry-webhook-delivery.md) for the provider-specific parameters and requirements.

