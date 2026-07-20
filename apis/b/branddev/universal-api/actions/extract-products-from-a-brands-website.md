# Brand.dev: Extract Products from a Brand's Website

Extracts product data from a brand website using Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-products-from-a-brands-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-products-from-a-brands-website?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-products-from-a-brands-website?${params}`, {
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
| `domain` | string | yes | Domain name to extract products from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "products": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `products[]` | array<object> |  |
| `products[].billingFrequency` | string |  |
| `products[].category` | string |  |
| `products[].currency` | string |  |
| `products[].description` | string |  |
| `products[].features[]` | array<string> |  |
| `products[].images[]` | array<string> |  |
| `products[].imageUrl` | string |  |
| `products[].name` | string |  |
| `products[].price` | number |  |
| `products[].pricingModel` | string |  |
| `products[].tags[]` | array<string> |  |
| `products[].targetAudience[]` | array<string> |  |
| `products[].url` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `POST /brand/ai/products` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-products-from-a-brands-website.md) for the provider-specific parameters and requirements.

