# Makeplans: Update Booking

Updates an existing booking in Makeplans.

```
PUT https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-booking', {
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
| `bookedFrom` | date | no | Booking start datetime. |
| `bookedTo` | date | no | Booking end datetime. |
| `bookingId` | number | yes | The Makeplans booking ID. |
| `resourceId` | number | no | Makeplans resource ID for the booking. |
| `title` | string | no | Optional booking title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "booked_from": "2026-05-07T12:00:00.000Z",
      "booked_to": "2026-05-07T12:00:00.000Z",
      "count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "notes": "string",
      "person_id": 1,
      "resource_id": 1,
      "service_id": 1,
      "state": "string",
      "status": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `booked_from` | date |  |
| `booked_to` | date |  |
| `count` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `notes` | string |  |
| `person_id` | number |  |
| `resource_id` | number |  |
| `service_id` | number |  |
| `state` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `PUT /bookings/:bookingId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking.md) for the provider-specific parameters and requirements.

