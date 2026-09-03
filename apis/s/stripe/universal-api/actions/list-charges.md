# Stripe: List Charges



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-charges?${params}`, {
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
| `customer` | string | no | Example: `cus_...`. |
| `paymentIntent` | string | no | Example: `pi_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountCaptured": 1,
      "amountRefunded": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "description": "string",
      "disputed": true,
      "id": "string",
      "outcome": {},
      "paid": true,
      "paymentIntent": "string",
      "paymentMethod": "string",
      "receiptUrl": "https://example.com",
      "refunded": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountCaptured` | number |  |
| `amountRefunded` | number |  |
| `created` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `description` | string |  |
| `disputed` | boolean |  |
| `id` | string |  |
| `outcome` | object |  |
| `paid` | boolean |  |
| `paymentIntent` | string |  |
| `paymentMethod` | string |  |
| `receiptUrl` | string |  |
| `refunded` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET charges` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-charges.md) for the provider-specific parameters and requirements.

