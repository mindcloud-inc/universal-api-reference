# Reloadify: Add Product To Order

Adds a product to an order in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "orderId": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "orderId": "string",
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `orderId` | string | yes | Order identifier. |
| `productId` | string | yes | Product identifier. |
| `quantity` | number | no | Quantity to attach to the order. |
| `variant_id` | string | no | Variant identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_attributes": [
        {}
      ],
      "order_id": "string",
      "product_id": "string",
      "quantity": 1,
      "variant_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_attributes` | array<object> |  |
| `order_id` | string |  |
| `product_id` | string |  |
| `quantity` | number |  |
| `variant_id` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/orders/:order_id/products/:product_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-product-to-order.md) for the provider-specific parameters and requirements.

