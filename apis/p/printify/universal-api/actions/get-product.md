# Printify: Get Product

Retrieves a product from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=69d9640a80a288b139051dcc&shopId=27141936" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "69d9640a80a288b139051dcc",
  "shopId": "27141936"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-product?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Printify product id. Default: `69d9640a80a288b139051dcc`. |
| `shopId` | number | yes | Printify shop id. Default: `27141936`. |

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

Through the native Printify API, this operation is `GET /shops/:shop_id/products/:product_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

