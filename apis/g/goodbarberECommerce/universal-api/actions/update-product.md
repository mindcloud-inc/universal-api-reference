# Goodbarber eCommerce: Update Product



```
PUT https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | Product ID. |
| `title` | string | no | Product title. |
| `summary` | string | no | Short product summary. |
| `status` | string | no | Product publication status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "collections": [
        {}
      ],
      "createdAt": "string",
      "id": 1,
      "productRef": "string",
      "showSimilarProducts": true,
      "slug": "string",
      "status": "string",
      "summary": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string | Product brand. |
| `collections` | array<object> | Assigned collections. |
| `createdAt` | string | Creation timestamp. |
| `id` | number | Product ID. |
| `productRef` | string | Merchant product reference. |
| `showSimilarProducts` | boolean | Whether related products are shown. |
| `slug` | string | Product slug. |
| `status` | string | Product status. |
| `summary` | string | Short product summary. |
| `tags` | array<string> | Product tags. |
| `title` | string | Product title. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `PATCH /publicapi/v2/general/catalog/:webzine_id/product/:product_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

