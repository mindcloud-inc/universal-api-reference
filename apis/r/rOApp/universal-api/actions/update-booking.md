# RO App: Update Booking



```
PUT https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingId` | number | yes | Booking ID |
| `branchId` | number | no | Location ID |
| `statusId` | number | no | Booking status ID (1: New, 2: Confirmed, 3: Pending, 4; In progress, 5: Completed 6 - Canceled, 7: No-show) |
| `assigneeId` | number | no | Assigned employee ID |
| `clientId` | number | no | Client (Person / Organization) ID |
| `scheduledFor` | date | no | "Scheduled From" date and time (ISO 8601) |
| `scheduledTo` | date | no | "Scheduled To" date and time (ISO 8601) |
| `resourceId` | number | no | Resource ID |
| `comment` | string | no | Comment text |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee_id": 1,
      "branch_id": 1,
      "client_id": 1,
      "comment": "string",
      "resource_id": 1,
      "scheduled_for": "2026-05-07T12:00:00.000Z",
      "scheduled_to": "2026-05-07T12:00:00.000Z",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee_id` | number |  |
| `branch_id` | number |  |
| `client_id` | number |  |
| `comment` | string |  |
| `resource_id` | number |  |
| `scheduled_for` | date |  |
| `scheduled_to` | date |  |
| `status_id` | number |  |

## Native endpoint

Through the native RO App API, this operation is `PATCH /bookings/:booking_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking.md) for the provider-specific parameters and requirements.

