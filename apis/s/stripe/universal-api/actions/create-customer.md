# Stripe: Create Customer

Creates a new customer in Stripe.

```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `description` | string | no |  |
| `metadata` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentMethod` | string | no |  |
| `source` | string | no |  |
| `address` | object | no |  |
| `shipping` | object | no |  |
| `taxExempt` | list<string> | no | One of: `exempt`, `none`, `reverse`. |
| `balance` | number | no |  |
| `cashBalance` | object | no |  |
| `invoicePrefix` | string | no |  |
| `invoiceSettings` | object | no |  |
| `nextInvoiceSequence` | number | no |  |
| `preferredLocales[]` | array<string> | no |  |
| `tax` | object | no |  |
| `taxIdData[]` | array<object> | no |  |
| `testClock` | string | no |  |
| `expand[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "currency": "string",
      "delinquent": true,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Default currency |
| `delinquent` | boolean | Whether the customer is delinquent |
| `email` | string | Customer email |
| `id` | string | Customer ID |
| `name` | string | Customer name |
| `object` | string | Stripe object type |

## Native endpoint

Through the native Stripe API, this operation is `POST customers` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

