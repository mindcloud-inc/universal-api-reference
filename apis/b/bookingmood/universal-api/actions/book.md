# Bookingmood: Book

Creates a booking in Bookingmood from product, interval, occupancy, and form values.

```
POST https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/book" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "interval.end": "string",
  "interval.start": "string",
  "occupancy": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/book', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "interval.end": "string",
    "interval.start": "string",
    "occupancy": "string",
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `couponCodes` | string | no | Coupon codes entered for the booking. |
| `currency` | string | no | Currency to use for the booking. |
| `formValues` | string | no | Values for the booking form fields. |
| `interval.end` | string | yes | End date for the booking interval. |
| `interval.start` | string | yes | Start date for the booking interval. |
| `occupancy` | string | yes | Occupancy per capacity group. |
| `productId` | string | yes | The identifier of the unit to book. |
| `showPendingAs` | string | no | How to interpret pending events when checking booking availability. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "booking_id": "string",
      "payment_url": "https://example.com",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking_id` | string |  |
| `payment_url` | string |  |
| `reference` | string |  |

## Native endpoint

Through the native Bookingmood API, this operation is `POST /book` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/book.md) for the provider-specific parameters and requirements.

