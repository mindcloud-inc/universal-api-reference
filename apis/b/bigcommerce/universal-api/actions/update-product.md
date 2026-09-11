# BigCommerce: Update Product



```
PUT https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "productId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "productId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A unique product name. |
| `productId` | string | yes |  |
| `type` | string | yes | The product type. One of: physical - a physical stock unit, digital - a digital download. |
| `sku` | string | no | A unique user-defined alphanumeric product code/stock keeping unit (SKU) |
| `weight` | number | no | Weight of the product, which can be used when calculating shipping costs. This is based on the unit set on the store |
| `price` | number | no | The price of the product. The price should include or exclude tax, based on the store settings |
| `isVisible` | boolean | no | Flag to determine whether the product should be displayed to customers browsing the store. If true, the product will be displayed. If false, the product will be hidden from view |
| `inventory_level` | number | no | The amount in inventory |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `PUT /v3/catalog/products/:productId` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

