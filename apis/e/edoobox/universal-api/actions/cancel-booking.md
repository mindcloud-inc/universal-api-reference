# Edoobox: Cancel Booking

Cancels an existing booking in Edoobox.

```
PUT https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/cancel-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/cancel-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": "booking_example",
  "offer": "offer_ac159e317af1_7511348589"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/cancel-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": "booking_example",
    "offer": "offer_ac159e317af1_7511348589"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingId` | string | yes | edoobox booking ID. Default: `booking_example`. |
| `offer` | string | yes | edoobox offer ID associated with the booking. Default: `offer_ac159e317af1_7511348589`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancel": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancel` | boolean | Whether the booking was cancelled. |
| `id` | string | The booking ID returned by edoobox. |

## Native endpoint

Through the native Edoobox API, this operation is `PUT /booking/:booking_id/cancel` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-booking.md) for the provider-specific parameters and requirements.

