# BaseLinker: Add Order Product

Adds a product to an order in BaseLinker.

```
POST https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/add-order-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/add-order-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/add-order-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_id` | number | yes | Order identifier to append a product to. |
| `storage` | string | no | Inventory source code for the product. |
| `storage_id` | number | no | Inventory source identifier for the product. |
| `product_id` | number | no | Product identifier from the selected storage. |
| `variant_id` | number | no | Variant identifier from the selected product. |
| `name` | string | no | Product name to add to the order. |
| `price_brutto` | number | no | Gross item price. |
| `quantity` | number | no | Quantity to add to the order. |
| `tax_rate` | number | no | VAT rate percentage for the item. |
| `attributes` | object | no | Product attributes payload for the order item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | object | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderProductId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderProductId` | number | Identifier of the item added to the order. |
| `status` | string | SUCCESS when the order item was added. |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-order-product.md) for the provider-specific parameters and requirements.

