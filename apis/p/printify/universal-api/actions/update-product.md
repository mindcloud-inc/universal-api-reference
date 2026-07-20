# Printify: Update Product

Updates a product in Printify.

```
PUT https://connect.mindcloud.co/v1/universal/printify/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printify/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product_id": "69d9640a80a288b139051dcc",
  "shop_id": "27141936"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/update-product', {
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
| `title` | string | no | Updated product title. Default: `MindCloud Printify Test Tee Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprintId": 1,
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "isLocked": true,
      "printProviderId": 1,
      "shopId": 1,
      "title": "string",
      "updatedAt": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprintId` | number |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `printProviderId` | number |  |
| `shopId` | number |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Printify API, this operation is `PUT /shops/:shop_id/products/:product_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

