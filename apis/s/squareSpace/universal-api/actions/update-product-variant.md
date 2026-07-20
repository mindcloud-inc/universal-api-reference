# SquareSpace: Update Product Variant

Updates a product variant in Squarespace.

```
PUT https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "variantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product-variant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "variantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | list<string> | yes | Product ID. |
| `variantId` | list<string> | yes | Variant ID. |

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

Through the native SquareSpace API, this operation is `POST /v2/commerce/products/:productId/variants/:variantId` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-variant.md) for the provider-specific parameters and requirements.

