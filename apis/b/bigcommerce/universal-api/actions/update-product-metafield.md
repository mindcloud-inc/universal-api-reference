# BigCommerce: Update Product Metafield



```
PUT https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-metafield
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-metafield" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "key": "string",
  "value": "string",
  "namespace": "Ava Chen",
  "permissionSet": "string",
  "metafieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-metafield', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "key": "string",
    "value": "string",
    "namespace": "Ava Chen",
    "permissionSet": "string",
    "metafieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes |  |
| `key` | string | yes |  |
| `value` | string | yes |  |
| `namespace` | string | yes |  |
| `permissionSet` | list<string> | yes |  |
| `description` | string | no |  |
| `metafieldId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `PUT /v3/catalog/products/:productId/metafields/:metafieldId` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-metafield.md) for the provider-specific parameters and requirements.

