# Reloadify: List Brand Products

Retrieves products for a brand in Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brand-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brand-products?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string&brandId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "languageId": "string",
  "brandId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brand-products?${params}`, {
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
| `languageId` | string | yes | Reloadify language ID. |
| `brandId` | string | yes | Brand identifier. |

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
      "custom_attributes": [
        {}
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
| `custom_attributes` | array<object> |  |
| `id` | string |  |
| `main_image` | string |  |
| `name` | string |  |
| `price` | number |  |
| `relevant_product_ids` | array<string> |  |
| `short_description` | string |  |
| `url` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/brands/:brand_id/products` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-brand-products.md) for the provider-specific parameters and requirements.

