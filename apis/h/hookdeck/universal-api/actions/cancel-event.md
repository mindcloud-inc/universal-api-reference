# Hookdeck: Cancel Event

Cancels a pending event in Hookdeck.

```
PUT https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/cancel-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/cancel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/cancel-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Hookdeck event ID from the `id` path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempts": 1,
      "cli_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "destination_id": "string",
      "error_code": "string",
      "event_data_id": "string",
      "id": "string",
      "last_attempt_at": "2026-05-07T12:00:00.000Z",
      "next_attempt_at": "2026-05-07T12:00:00.000Z",
      "request_id": "string",
      "response_status": 1,
      "source_id": "string",
      "status": "string",
      "successful_at": "2026-05-07T12:00:00.000Z",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "webhook_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempts` | number |  |
| `cli_id` | string |  |
| `created_at` | date |  |
| `data` | object |  |
| `destination_id` | string |  |
| `error_code` | string |  |
| `event_data_id` | string |  |
| `id` | string |  |
| `last_attempt_at` | date |  |
| `next_attempt_at` | date |  |
| `request_id` | string |  |
| `response_status` | number |  |
| `source_id` | string |  |
| `status` | string |  |
| `successful_at` | date |  |
| `team_id` | string |  |
| `updated_at` | date |  |
| `webhook_id` | string |  |

## Native endpoint

Through the native Hookdeck API, this operation is `PUT /events/:id/cancel` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-event.md) for the provider-specific parameters and requirements.

