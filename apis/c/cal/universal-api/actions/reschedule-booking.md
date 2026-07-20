# Cal.com: Reschedule Booking

Updates a booking in Cal.com by rescheduling it.

```
PUT https://connect.mindcloud.co/v1/universal/cal/latest/actions/reschedule-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cal/latest/actions/reschedule-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingUid": "string",
  "start": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/reschedule-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingUid": "string",
    "start": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingUid` | list | yes | Booking identifier from Cal.com path parameter. |
| `start` | string | yes | New booking start time in ISO 8601 UTC format. |
| `reschedulingReason` | string | no | Reason text describing why the booking is being rescheduled. |
| `rescheduledBy` | string | no | Identifier for the actor who requested the reschedule. |
| `seatUid` | string | no | Seat booking UID when rescheduling a seat booking. |
| `emailVerificationCode` | string | no | Email verification code for protected event types. |

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

Through the native Cal.com API, this operation is `POST /bookings/:bookingUid/reschedule` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-booking.md) for the provider-specific parameters and requirements.

