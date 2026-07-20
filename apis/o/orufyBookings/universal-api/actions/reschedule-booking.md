# Orufy Bookings: Reschedule Booking



```
PUT https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/reschedule-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/reschedule-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attendeeId": "string",
  "meetId": "string",
  "timezone": "string",
  "time[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/reschedule-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attendeeId": "string",
    "meetId": "string",
    "timezone": "string",
    "time[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attendeeId` | string | yes | The attendee identifier returned by Get Booking Queue Status or Reschedule Booking. |
| `meetId` | string | yes | The meet identifier returned by Get Booking Queue Status or Reschedule Booking. |
| `timezone` | string | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `time[]` | array<object> | yes | An array of time objects. Each item must include a `time` ISO datetime value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendee": {},
      "isSuccess": true,
      "meet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendee` | object |  |
| `isSuccess` | boolean |  |
| `meet` | array<object> |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `PATCH /meet/reschedule` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-booking.md) for the provider-specific parameters and requirements.

