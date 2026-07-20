# G2: Get Product

Retrieves a product from G2.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-product?${params}`, {
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
| `productId` | string | yes | Product UUID or slug from the G2 API spec. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "detailDescription": "string",
        "domain": "string",
        "g2Url": "https://example.com",
        "imageUrl": "https://example.com",
        "name": "Ava Chen",
        "pricingTiers": [
          "string"
        ],
        "publicDetailUrl": "https://example.com",
        "reviewCount": 1,
        "slug": "string",
        "starRating": 1,
        "type": "string",
        "writeReviewUrl": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.detailDescription` | string |  |
| `attributes.domain` | string |  |
| `attributes.g2Url` | string |  |
| `attributes.imageUrl` | string |  |
| `attributes.name` | string |  |
| `attributes.pricingTiers[]` | string |  |
| `attributes.publicDetailUrl` | string |  |
| `attributes.reviewCount` | number |  |
| `attributes.slug` | string |  |
| `attributes.starRating` | number |  |
| `attributes.type` | string |  |
| `attributes.writeReviewUrl` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native G2 API, this operation is `GET /api/v2/products/:product_id` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

