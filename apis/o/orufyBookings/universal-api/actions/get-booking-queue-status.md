# Orufy Bookings: Get Booking Queue Status



```
GET https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-booking-queue-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-booking-queue-status?connectionId=$CONNECTION_ID&queueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-booking-queue-status?${params}`, {
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
| `queueId` | string | yes | The queue identifier returned by Create Booking. |

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
      ],
      "queueStatus": "string",
      "redirectUrl": "https://example.com"
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
| `queueStatus` | string |  |
| `redirectUrl` | string |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `GET /meet/queue-event/status/:queueId` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-queue-status.md) for the provider-specific parameters and requirements.

