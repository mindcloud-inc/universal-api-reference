# Cal.com: Add Booking Guests

Updates a booking in Cal.com by adding guests.

```
PUT https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-guests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-guests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingUid": "string",
  "guests[]": [
    {}
  ],
  "guests[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/add-booking-guests', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingUid": "string",
    "guests[]": [{}],
    "guests[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingUid` | list | yes | Booking identifier from Cal.com path parameter. |
| `guests[]` | array<object> | yes | Array of guest objects to add to the booking. |
| `guests[].email` | string | yes | Guest email address. |
| `guests[].name` | string | no | Guest display name. |
| `guests[].timeZone` | string | no | Guest IANA time zone. |
| `guests[].phoneNumber` | string | no | Guest phone number. |
| `guests[].language` | string | no | Guest language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "duration": 1,
      "end": "string",
      "eventTypeId": 1,
      "guests": [
        "string"
      ],
      "id": 1,
      "location": "string",
      "meetingUrl": "https://example.com",
      "metadata": {},
      "start": "string",
      "status": "string",
      "title": "string",
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `end` | string |  |
| `eventTypeId` | number |  |
| `guests` | array<string> |  |
| `id` | number |  |
| `location` | string |  |
| `meetingUrl` | string |  |
| `metadata` | object |  |
| `start` | string |  |
| `status` | string |  |
| `title` | string |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `POST /bookings/:bookingUid/guests` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-booking-guests.md) for the provider-specific parameters and requirements.

