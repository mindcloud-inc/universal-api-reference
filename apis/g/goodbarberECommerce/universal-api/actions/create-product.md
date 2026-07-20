# Goodbarber eCommerce: Create Product



```
POST https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collections[]": [
    1
  ],
  "tags[]": [
    "string"
  ],
  "setCustomSimilarProducts[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collections[]": [1],
    "tags[]": ["string"],
    "setCustomSimilarProducts[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Product title. |
| `summary` | string | no | Short product summary. |
| `status` | string | no | Product publication status. |
| `slug` | string | no | Product slug. |
| `showSimilarProducts` | boolean | no | Whether related products should be shown. |
| `collections[]` | array<number> | yes | Collection IDs assigned to the product. |
| `tags[]` | array<string> | yes | Tags assigned to the product. |
| `setCustomSimilarProducts[]` | array<number> | yes | Explicit related product IDs. |

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

Through the native Goodbarber eCommerce API, this operation is `POST /publicapi/v2/general/catalog/:webzine_id/product/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

