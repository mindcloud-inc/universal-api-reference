# Reloadify: Get Product

Retrieves a product from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-product?connectionId=$CONNECTION_ID&language_id=string&product_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language_id": "string",
  "product_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-product?${params}`, {
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
| `language_id` | string | yes | Language ID from the Reloadify language resource. |
| `product_id` | string | yes | Product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand_id": "string",
      "category_ids": [
        "string"
      ],
      "id": "string",
      "main_image": "string",
      "name": "Ava Chen",
      "price": 1,
      "relevant_product_ids": [
        "string"
      ],
      "short_description": "string",
      "url": "https://example.com",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand_id` | string |  |
| `category_ids` | array<string> |  |
| `id` | string |  |
| `main_image` | string |  |
| `name` | string |  |
| `price` | number |  |
| `relevant_product_ids` | array<string> |  |
| `short_description` | string |  |
| `url` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/products/:product_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

