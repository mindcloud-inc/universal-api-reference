# RO App: Get Booking



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-booking?${params}`, {
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
| `bookingId` | number | yes | Booking ID |

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

Through the native RO App API, this operation is `GET /bookings/:booking_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

