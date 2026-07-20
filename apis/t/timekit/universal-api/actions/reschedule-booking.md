# Timekit: Reschedule Booking



```
PUT https://connect.mindcloud.co/v1/universal/timekit/latest/actions/reschedule-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/reschedule-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "end": "string",
  "id": "string",
  "resourceId": "string",
  "start": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timekit/latest/actions/reschedule-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "end": "string",
    "id": "string",
    "resourceId": "string",
    "start": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | string | yes |  |
| `id` | string | yes |  |
| `resourceId` | string | yes |  |
| `start` | string | yes |  |

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

Through the native Timekit API, this operation is `POST /bookings/:id/reschedule` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-booking.md) for the provider-specific parameters and requirements.

