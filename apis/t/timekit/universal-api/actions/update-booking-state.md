# Timekit: Update Booking State

Updates a booking's state in Timekit.

```
PUT https://connect.mindcloud.co/v1/universal/timekit/latest/actions/update-booking-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/update-booking-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "cancel",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timekit/latest/actions/update-booking-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "cancel",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | list<string> | yes | One of: `cancel`, `cancel_by_customer`, `complete`, `confirm`, `decline`. |
| `applyToBulkedBookings` | boolean | no | Default: `false`. |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "graph": "string",
      "id": "string",
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean |  |
| `created_at` | date |  |
| `graph` | string |  |
| `id` | string |  |
| `state` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Timekit API, this operation is `PUT /bookings/:id/:action` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking-state.md) for the provider-specific parameters and requirements.

