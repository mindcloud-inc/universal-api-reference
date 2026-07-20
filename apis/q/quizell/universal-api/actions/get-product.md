# Quizell: Get Product

Retrieves a product from Quizell by ID.

```
GET https://connect.mindcloud.co/v1/universal/quizell/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quizell/latest/actions/get-product?${params}`, {
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
| `productId` | number | yes | The ID of the product to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bullet_description": "string",
      "collections": [
        {}
      ],
      "compare_at_price": 1,
      "created_at": "string",
      "description": "string",
      "detail_link": "https://example.com",
      "id": 1,
      "image": "string",
      "images": [
        {}
      ],
      "price": "string",
      "sku": "string",
      "status": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "updated_at": "string",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bullet_description` | string |  |
| `collections` | array<object> |  |
| `compare_at_price` | number |  |
| `created_at` | string |  |
| `description` | string |  |
| `detail_link` | string |  |
| `id` | number |  |
| `image` | string |  |
| `images` | array<object> |  |
| `price` | string |  |
| `sku` | string |  |
| `status` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `updated_at` | string |  |
| `vendor` | string |  |

## Native endpoint

Through the native Quizell API, this operation is `GET /products/:product_id/show` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

