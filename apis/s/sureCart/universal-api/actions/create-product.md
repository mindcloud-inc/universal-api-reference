# SureCart: Create Product



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product.name": "Test Product"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product.name": "Test Product"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product.name` | string | yes | The product display name. Example: `Test Product`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowOutOfStockPurchases": true,
      "archived": true,
      "autoFulfillEnabled": true,
      "availableStock": 1,
      "averageStars": "string",
      "catalogedAt": 1,
      "createdAt": 1,
      "description": "string",
      "dimensions": {
        "height": 1,
        "length": 1,
        "unit": "string",
        "width": 1
      },
      "featured": true,
      "id": "string",
      "imageUrl": "https://example.com",
      "licensingEnabled": true,
      "metrics": {
        "currency": "string",
        "maxPriceAmount": 1,
        "minPriceAmount": 1,
        "pricesCount": 1
      },
      "name": "Ava Chen",
      "object": "string",
      "recurring": true,
      "reviewsEnabled": true,
      "shippingEnabled": true,
      "shippingProfile": "string",
      "sku": "string",
      "slug": "string",
      "solicitReviews": true,
      "status": "string",
      "stock": 1,
      "stockEnabled": true,
      "taxCategory": "string",
      "taxEnabled": true,
      "updatedAt": 1,
      "weight": 1,
      "weightUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowOutOfStockPurchases` | boolean |  |
| `archived` | boolean |  |
| `autoFulfillEnabled` | boolean |  |
| `availableStock` | number |  |
| `averageStars` | string |  |
| `catalogedAt` | number |  |
| `createdAt` | number |  |
| `description` | string |  |
| `dimensions.height` | number |  |
| `dimensions.length` | number |  |
| `dimensions.unit` | string |  |
| `dimensions.width` | number |  |
| `featured` | boolean |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `licensingEnabled` | boolean |  |
| `metrics.currency` | string |  |
| `metrics.maxPriceAmount` | number |  |
| `metrics.minPriceAmount` | number |  |
| `metrics.pricesCount` | number |  |
| `name` | string |  |
| `object` | string |  |
| `recurring` | boolean |  |
| `reviewsEnabled` | boolean |  |
| `shippingEnabled` | boolean |  |
| `shippingProfile` | string |  |
| `sku` | string |  |
| `slug` | string |  |
| `solicitReviews` | boolean |  |
| `status` | string |  |
| `stock` | number |  |
| `stockEnabled` | boolean |  |
| `taxCategory` | string |  |
| `taxEnabled` | boolean |  |
| `updatedAt` | number |  |
| `weight` | number |  |
| `weightUnit` | string |  |

## Native endpoint

Through the native SureCart API, this operation is `POST v1/products` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

