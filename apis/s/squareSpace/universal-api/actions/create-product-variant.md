# SquareSpace: Create Product Variant

Creates a product variant in Squarespace.

```
POST https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-product-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-product-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "sku": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-product-variant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "sku": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<string> | yes | Product ID. |
| `pricing.basePrice.currency` | string | no | Variant base price currency (ISO code). |
| `pricing.basePrice.value` | string | no | Variant base price amount. |
| `sku` | string | yes | Variant SKU code. |
| `stock.quantity` | number | no | Finite stock quantity. |
| `stock.unlimited` | boolean | no | Whether stock is unlimited. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "image": {},
      "pricing": {},
      "shippingMeasurements": {},
      "sku": "string",
      "stock": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `image` | object |  |
| `pricing` | object |  |
| `shippingMeasurements` | object |  |
| `sku` | string |  |
| `stock` | object |  |

## Native endpoint

Through the native SquareSpace API, this operation is `POST /v2/commerce/products/:id/variants` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-variant.md) for the provider-specific parameters and requirements.

