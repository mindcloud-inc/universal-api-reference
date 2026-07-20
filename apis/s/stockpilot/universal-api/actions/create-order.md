# Stockpilot: Create Order

Creates a new order in Stockpilot.

```
POST https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billing": {},
  "billing.firstname": "Ava",
  "billing.lastname": "Chen",
  "billing.zipcode": "string",
  "billing.country": "string",
  "shipping": {},
  "shipping.firstname": "Ava",
  "shipping.lastname": "Chen",
  "shipping.zipcode": "string",
  "shipping.country": "string",
  "customerEmail": "ava@example.com",
  "line_items[]": [
    {}
  ],
  "line_items[].product_id": "string",
  "line_items[].price": "string",
  "line_items[].quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billing": {},
    "billing.firstname": "Ava",
    "billing.lastname": "Chen",
    "billing.zipcode": "string",
    "billing.country": "string",
    "shipping": {},
    "shipping.firstname": "Ava",
    "shipping.lastname": "Chen",
    "shipping.zipcode": "string",
    "shipping.country": "string",
    "customerEmail": "ava@example.com",
    "line_items[]": [{}],
    "line_items[].product_id": "string",
    "line_items[].price": "string",
    "line_items[].quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billing` | object | yes |  |
| `billing.address2` | string | no |  |
| `billing.city` | string | no |  |
| `billing.company` | string | no |  |
| `billing.houseNumber` | string | no |  |
| `billing.region` | string | no |  |
| `billing.street` | string | no |  |
| `billing.suffix` | string | no |  |
| `customerNote` | string | no |  |
| `customerPhone` | string | no |  |
| `shipping.address2` | string | no |  |
| `shipping.city` | string | no |  |
| `shipping.company` | string | no |  |
| `shipping.houseNumber` | string | no |  |
| `shipping.region` | string | no |  |
| `shipping.street` | string | no |  |
| `shipping.suffix` | string | no |  |
| `shippingMethod` | string | no |  |
| `shippingTotal` | string | no |  |
| `vatNumber` | string | no |  |
| `billing.firstname` | string | yes |  |
| `billing.lastname` | string | yes |  |
| `billing.zipcode` | string | yes |  |
| `billing.country` | string | yes |  |
| `shipping` | object | yes |  |
| `shipping.firstname` | string | yes |  |
| `shipping.lastname` | string | yes |  |
| `shipping.zipcode` | string | yes |  |
| `shipping.country` | string | yes |  |
| `customerEmail` | string | yes |  |
| `line_items[]` | array<object> | yes |  |
| `line_items[].product_id` | string | yes |  |
| `line_items[].price` | string | yes |  |
| `line_items[].quantity` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order_id": "string",
      "pk": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order_id` | string |  |
| `pk` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /orders/create` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

