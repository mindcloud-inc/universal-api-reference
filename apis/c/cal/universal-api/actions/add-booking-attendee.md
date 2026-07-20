# Cal.com: Add Booking Attendee

Updates a booking in Cal.com by adding an attendee.

```
PUT https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-attendee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-attendee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingUid": "string",
  "name": "Ava Chen",
  "timeZone": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-attendee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingUid": "string",
    "name": "Ava Chen",
    "timeZone": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingUid` | list | yes | Booking identifier from Cal.com path parameter. |
| `name` | string | yes | Attendee full name. |
| `timeZone` | string | yes | Attendee IANA time zone. |
| `email` | string | yes | Attendee email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absent": true,
      "bookingId": 1,
      "displayEmail": "ava@example.com",
      "email": "ava@example.com",
      "id": 1,
      "language": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absent` | boolean |  |
| `bookingId` | number |  |
| `displayEmail` | string |  |
| `email` | string |  |
| `id` | number |  |
| `language` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `POST /bookings/:bookingUid/attendees` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-booking-attendee.md) for the provider-specific parameters and requirements.

