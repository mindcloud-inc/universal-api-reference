# Printify: Unpublish Product

Unpublishes a product in Printify.

```
PUT https://connect.mindcloud.co/v1/universal/printify/latest/actions/unpublish-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printify/latest/actions/unpublish-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product_id": "69d9640a80a288b139051dcc",
  "shop_id": "27141936"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/unpublish-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product_id": "69d9640a80a288b139051dcc",
    "shop_id": "27141936"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product_id` | string | yes | Printify product id. Default: `69d9640a80a288b139051dcc`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/products/:product_id/unpublish.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unpublish-product.md) for the provider-specific parameters and requirements.

