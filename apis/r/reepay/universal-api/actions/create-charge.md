# Reepay: Create Charge

Creates a new charge in Reepay.

```
POST https://connect.mindcloud.co/v1/universal/reepay/latest/actions/create-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/create-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/create-charge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string",
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_funding` | boolean | no |  |
| `account_funding_information` | object | no |  |
| `acquirer_reference` | string | no |  |
| `amount` | number | no |  |
| `async` | boolean | no |  |
| `billing_address` | object | no |  |
| `currency` | string | no |  |
| `customer` | object | no |  |
| `customer_handle` | string | no |  |
| `handle` | string | yes |  |
| `key` | string | no |  |
| `metadata` | object | no |  |
| `order_lines[]` | array<object> | no |  |
| `ordertext` | string | no |  |
| `parameters` | object | no |  |
| `payment_method_reference` | string | no |  |
| `recurring` | boolean | no |  |
| `settle` | boolean | no |  |
| `shipping_address` | object | no |  |
| `source` | string | yes |  |
| `text_on_statement` | string | no |  |
| `use_pm_for_subscription` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": "string",
      "handle": "string",
      "order_lines": [
        {
          "amount": 1,
          "ordertext": "string",
          "quantity": 1,
          "vat": 1
        }
      ],
      "refunded_amount": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created` | date |  |
| `currency` | string |  |
| `customer` | string |  |
| `handle` | string |  |
| `order_lines[].amount` | number |  |
| `order_lines[].ordertext` | string |  |
| `order_lines[].quantity` | number |  |
| `order_lines[].vat` | number |  |
| `refunded_amount` | number |  |
| `state` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `POST /v1/charge` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-charge.md) for the provider-specific parameters and requirements.

