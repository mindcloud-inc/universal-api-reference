# Hookdeck: Get Request Events

Retrieves events for a request in Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-request-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-request-events?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-request-events?${params}`, {
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
| `id` | string | yes | Hookdeck request ID from the `id` path parameter. |

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

Through the native Hookdeck API, this operation is `GET /requests/:id/events` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-request-events.md) for the provider-specific parameters and requirements.

