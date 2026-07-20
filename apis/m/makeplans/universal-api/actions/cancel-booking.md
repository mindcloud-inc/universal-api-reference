# Makeplans: Cancel Booking

Cancels an existing booking in Makeplans.

```
PUT https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/cancel-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/cancel-booking', {
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
| `bookingId` | number | yes | The Makeplans booking ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "booked_from": "2026-05-07T12:00:00.000Z",
      "booked_to": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "state": "string",
      "status": "string",
      "title": "string"
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
| `id` | number |  |
| `state` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Makeplans API, this operation is `PUT /bookings/:bookingId/cancel` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-booking.md) for the provider-specific parameters and requirements.

