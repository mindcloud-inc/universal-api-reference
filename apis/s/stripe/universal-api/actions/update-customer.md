# Stripe: Update Customer

Updates an existing customer in Stripe.

```
PUT https://connect.mindcloud.co/v1/universal/stripe/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes | The ID of the customer to update. |
| `name` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `description` | string | no |  |
| `metadata` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `defaultSource` | string | no |  |
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
| `defaultBankAccount` | string | no |  |
| `defaultCard` | string | no |  |
| `defaultAlipayAccount` | string | no |  |
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

Through the native Stripe API, this operation is `POST customers/:customer` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

