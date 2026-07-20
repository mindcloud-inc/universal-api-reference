# Timekit: Create Booking

Creates a new booking in Timekit.

```
POST https://connect.mindcloud.co/v1/universal/timekit/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": {},
  "description": "string",
  "end": "string",
  "graph": "string",
  "resourceId": "string",
  "start": "string",
  "what": "string",
  "where": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timekit/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": {},
    "description": "string",
    "end": "string",
    "graph": "string",
    "resourceId": "string",
    "start": "string",
    "what": "string",
    "where": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarId` | string | no |  |
| `customer` | object | yes |  |
| `description` | string | yes |  |
| `end` | string | yes |  |
| `graph` | string | yes |  |
| `includes` | string | no |  |
| `invite` | boolean | no |  |
| `meta` | object | no |  |
| `myRsvp` | string | no |  |
| `participants[]` | array<string> | no |  |
| `projectId` | string | no |  |
| `reservationId` | string | no |  |
| `resourceId` | string | yes |  |
| `settings` | object | no |  |
| `start` | string | yes |  |
| `what` | string | yes |  |
| `where` | string | yes |  |

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

Through the native Timekit API, this operation is `POST /bookings` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

