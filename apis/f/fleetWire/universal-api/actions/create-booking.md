# FleetWire: Create Booking

Creates a new booking in FleetWire.

```
POST https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "version": "v2",
  "listingId": "string",
  "start": "string",
  "end": "string",
  "customerFirstName": "Ava",
  "customerLastName": "Chen",
  "customerEmail": "ava@example.com",
  "customerPhone": "string",
  "isPrimaryCustomer": true,
  "customerPhoneNumber": "string",
  "agreeToTerms": true,
  "customerDob": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "version": "v2",
    "listingId": "string",
    "start": "string",
    "end": "string",
    "customerFirstName": "Ava",
    "customerLastName": "Chen",
    "customerEmail": "ava@example.com",
    "customerPhone": "string",
    "isPrimaryCustomer": true,
    "customerPhoneNumber": "string",
    "agreeToTerms": true,
    "customerDob": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | string | yes | FleetWire checkout API version. Default: `v2`. |
| `listingId` | string | yes | FleetWire listing ID for the booking. |
| `start` | string | yes | Checkout start datetime. |
| `end` | string | yes | Checkout end datetime. |
| `customerFirstName` | string | yes | Primary customer first name. |
| `customerLastName` | string | yes | Primary customer last name. |
| `customerEmail` | string | yes | Primary customer email. |
| `customerPhone` | string | yes | Primary customer phone number. |
| `isPrimaryCustomer` | boolean | yes | Whether this customer is the primary renter. |
| `customerPhoneNumber` | string | yes | Primary customer phone number in the phone_number field. |
| `agreeToTerms` | boolean | yes | Whether the customer agrees to the terms. |
| `customerDob` | string | yes | Primary customer date of birth in YYYY-MM-DD format. |
| `customerAge` | string | no | Primary customer age if required by the tenant checkout validation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "b_id": "string",
      "customer": {},
      "l_id": "string",
      "p_id": "string",
      "stripePaymentIntent": {},
      "stripeSession": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `b_id` | string | Created FleetWire booking identifier. |
| `customer` | object | Created or matched FleetWire customer record. |
| `l_id` | string | Listing ID used for the checkout. |
| `p_id` | string | FleetWire payment or planning identifier returned by checkout. |
| `stripePaymentIntent` | object | Stripe payment intent payload when present. |
| `stripeSession` | object | Stripe session payload when present. |
| `success` | boolean | Whether FleetWire created the checkout successfully. |

## Native endpoint

Through the native FleetWire API, this operation is `POST /api/v1/checkout` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

