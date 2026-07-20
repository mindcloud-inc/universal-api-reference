# Stripe: List Payment Intents

Retrieves payment intents from your Stripe account.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-payment-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-payment-intents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-payment-intents?${params}`, {
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
| `limit` | number | no |  |
| `customer` | string | no | Only return PaymentIntents for this customer ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startingAfter` | string | no |  |
| `endingBefore` | string | no |  |
| `created` | object | no | Filter by creation timestamp or range object. |
| `customerAccount` | string | no |  |
| `expand[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountReceived": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "id": "string",
      "object": "string",
      "paymentMethod": "string",
      "paymentMethodTypes": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Requested amount |
| `amountReceived` | number | Received amount |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Payment currency |
| `customer` | string | Customer ID |
| `id` | string | Payment intent ID |
| `object` | string | Stripe object type |
| `paymentMethod` | string | Payment method ID |
| `paymentMethodTypes` | array<string> | Allowed payment method types |
| `status` | string | Payment intent status |

## Native endpoint

Through the native Stripe API, this operation is `GET payment_intents` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-intents.md) for the provider-specific parameters and requirements.

