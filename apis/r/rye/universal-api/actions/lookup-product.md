# Rye: Lookup Product

Finds a product in Rye by URL.

```
GET https://connect.mindcloud.co/v1/universal/rye/latest/actions/lookup-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/lookup-product?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/lookup-product?${params}`, {
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
| `url` | string | yes | The product URL to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "brand": "string",
      "description": "string",
      "id": "string",
      "images": [
        {}
      ],
      "isPurchasable": true,
      "name": "Ava Chen",
      "price": {},
      "sku": "string",
      "url": "https://example.com",
      "variantDimensions": [
        {}
      ],
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | string |  |
| `brand` | string |  |
| `description` | string |  |
| `id` | string |  |
| `images` | array<object> |  |
| `isPurchasable` | boolean |  |
| `name` | string |  |
| `price` | object |  |
| `sku` | string |  |
| `url` | string |  |
| `variantDimensions` | array<object> |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native Rye API, this operation is `GET /api/v1/products/lookup` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-product.md) for the provider-specific parameters and requirements.

