# Voog: Update Product

Updates an existing product in the current Voog store.

```
PUT https://connect.mindcloud.co/v1/universal/voog/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voog/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "price": 1,
  "productId": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voog/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "price": 1,
    "productId": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Updated product name. |
| `price` | number | yes | Updated product price. |
| `productId` | number | yes | Numeric product ID. |
| `status` | string | yes | Updated product status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voog API returns.

## Native endpoint

Through the native Voog API, this operation is `PUT /ecommerce/v1/products/:productId` (base URL `{{credentials.siteUrl}}/admin/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

