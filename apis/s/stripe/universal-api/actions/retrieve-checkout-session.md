# Stripe: Retrieve Checkout Session

Retrieves a checkout session from Stripe.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-checkout-session?connectionId=$CONNECTION_ID&session=cs_test_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session": "cs_test_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-checkout-session?${params}`, {
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
| `session` | string | yes | Checkout session ID to retrieve. Example: `cs_test_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountTotal": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "paymentStatus": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountTotal` | number | Total amount |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Session currency |
| `customer` | string | Customer ID |
| `id` | string | Checkout session ID |
| `mode` | string | Checkout mode |
| `object` | string | Stripe object type |
| `paymentStatus` | string | Payment status |
| `status` | string | Session status |
| `url` | string | Hosted checkout URL |

## Native endpoint

Through the native Stripe API, this operation is `GET checkout/sessions/:session` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-checkout-session.md) for the provider-specific parameters and requirements.

