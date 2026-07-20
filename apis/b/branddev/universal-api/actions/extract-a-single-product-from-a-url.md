# Brand.dev: Extract a Single Product from a URL

Extracts product data from a URL using Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-a-single-product-from-a-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-a-single-product-from-a-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-a-single-product-from-a-url?${params}`, {
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
| `url` | string | yes | Product page URL to extract product data from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isProductPage": true,
      "platform": "string",
      "product": {
        "billingFrequency": "string",
        "category": "string",
        "currency": "string",
        "description": "string",
        "features": [
          [
            "string"
          ]
        ],
        "images": [
          [
            "string"
          ]
        ],
        "imageUrl": "https://example.com",
        "name": "Ava Chen",
        "price": 1,
        "pricingModel": "string",
        "tags": [
          [
            "string"
          ]
        ],
        "targetAudience": [
          [
            "string"
          ]
        ],
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isProductPage` | boolean |  |
| `platform` | string |  |
| `product` | object |  |
| `product.billingFrequency` | string |  |
| `product.category` | string |  |
| `product.currency` | string |  |
| `product.description` | string |  |
| `product.features[]` | array<string> |  |
| `product.images[]` | array<string> |  |
| `product.imageUrl` | string |  |
| `product.name` | string |  |
| `product.price` | number |  |
| `product.pricingModel` | string |  |
| `product.tags[]` | array<string> |  |
| `product.targetAudience[]` | array<string> |  |
| `product.url` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `POST /brand/ai/product` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-a-single-product-from-a-url.md) for the provider-specific parameters and requirements.

