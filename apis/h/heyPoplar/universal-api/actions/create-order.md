# HeyPoplar: Create Order

Creates a new order in HeyPoplar.

```
POST https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "orderDate": "string",
  "customerEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "orderDate": "string",
    "customerEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | The unique identifier for this order. |
| `orderDate` | string | yes | ISO8601 purchase date in YYYY-MM-DD format. |
| `customerEmail` | string | yes | Customer email address. Poplar hashes it and discards the plaintext value. |
| `total` | number | no | Total order value as a decimal number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_address": {},
      "currency": "string",
      "customer": {},
      "id": "string",
      "metadata": {},
      "order_date": "string",
      "order_id": "string",
      "order_items": [
        {}
      ],
      "shipping_address": {},
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_address` | object |  |
| `currency` | string |  |
| `customer` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `order_date` | string |  |
| `order_id` | string |  |
| `order_items` | array<object> |  |
| `shipping_address` | object |  |
| `total` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `POST /order` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

