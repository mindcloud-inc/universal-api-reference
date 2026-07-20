# Beds24: List Stripe Payment Methods

Retrieves Stripe payment methods for a booking from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-stripe-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-stripe-payment-methods?connectionId=$CONNECTION_ID&bookingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-stripe-payment-methods?${params}`, {
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
| `bookingId` | number | yes | Beds24 booking ID whose Stripe payment methods should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stripePaymentMethod": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stripePaymentMethod` | object |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /channels/stripe/paymentMethods` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stripe-payment-methods.md) for the provider-specific parameters and requirements.

