# RO App: Create Booking



```
POST https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": 1,
  "assigneeId": 1,
  "clientId": 1,
  "scheduledFor": "2026-05-07T12:00:00.000Z",
  "scheduledTo": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": 1,
    "assigneeId": 1,
    "clientId": 1,
    "scheduledFor": "2026-05-07T12:00:00.000Z",
    "scheduledTo": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchId` | number | yes | Location ID |
| `assigneeId` | number | yes | Assigned Employee ID |
| `clientId` | number | yes | Client (Person / Organization) ID |
| `scheduledFor` | date | yes | "Scheduled From" date and time (ISO 8601) |
| `scheduledTo` | date | yes | "Scheduled To" date and time (ISO 8601) |
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

Through the native RO App API, this operation is `POST /bookings` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

