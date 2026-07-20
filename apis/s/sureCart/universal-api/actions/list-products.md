# SureCart: List Products



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-products?${params}`, {
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
| `query` | string | no | Full-text search query for the product collection. Example: `codex`. |
| `archived` | boolean | no | Only return archived or active products. |
| `featured` | boolean | no | Only return featured or non-featured products. |
| `recurring` | boolean | no | Only return recurring or one-time products. |

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

Through the native SureCart API, this operation is `GET v1/products` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

