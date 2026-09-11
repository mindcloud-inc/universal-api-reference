# BigCommerce: Update Product Variant



```
PUT https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "price": 1,
  "variantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-variant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "price": 1,
    "variantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `price` | number | yes | The price of the product. The price should include or exclude tax, based on the store settings |
| `sku` | string | no | A unique user-defined alphanumeric product code/stock keeping unit (SKU) |
| `option_values[]` | array | no | Ex: "option_values": [ { "option_display_name": "Color", "label": "Beige", "id": 146, "option_id": 151 } ] |
| `productId` | string | no |  |
| `variantId` | string | yes |  |
| `inventory_level` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `PUT /v3/catalog/products/:productId/variants/:variantId` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-variant.md) for the provider-specific parameters and requirements.

