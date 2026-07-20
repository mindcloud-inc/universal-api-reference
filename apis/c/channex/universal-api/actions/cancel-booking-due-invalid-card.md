# Channex: Cancel Booking Due Invalid Card

Cancels a booking for an invalid card in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/cancel-booking-due-invalid-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/cancel-booking-due-invalid-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/cancel-booking-due-invalid-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingId` | string | yes | UUID of the booking to cancel due to an invalid card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.message` | string |  |

## Native endpoint

Through the native Channex API, this operation is `POST /bookings/:bookingId/cancel_due_invalid_card` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-booking-due-invalid-card.md) for the provider-specific parameters and requirements.

