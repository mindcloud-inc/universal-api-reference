# SuperSend: List Webhook Deliveries

Retrieves webhook deliveries from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-webhook-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-webhook-deliveries?connectionId=$CONNECTION_ID&id=string&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-webhook-deliveries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `teamId` | string | yes |  |
| `status` | string | no | Allowed values: pending, delivered, failed, retrying. |
| `eventType` | string | no |  |
| `campaignId` | string | no |  |
| `search` | string | no |  |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

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

Through the native SuperSend API, this operation is `GET /webhooks/{id}/deliveries` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-deliveries.md) for the provider-specific parameters and requirements.

