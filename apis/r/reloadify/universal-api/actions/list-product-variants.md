# Reloadify: List Product Variants

Retrieves product variants from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-product-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-product-variants?connectionId=$CONNECTION_ID&limit=25&offset=0&language_id=string&product_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "language_id": "string",
  "product_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-product-variants?${params}`, {
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
      "article_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "default": true,
      "ean": "string",
      "id": "string",
      "main_image": "string",
      "old_price_excl": 1,
      "old_price_incl": 1,
      "price_cost": 1,
      "price_excl": 1,
      "price_incl": 1,
      "product_id": "string",
      "sku": "string",
      "stock_level": 1,
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article_code` | string |  |
| `created_at` | date |  |
| `default` | boolean |  |
| `ean` | string |  |
| `id` | string |  |
| `main_image` | string |  |
| `old_price_excl` | number |  |
| `old_price_incl` | number |  |
| `price_cost` | number |  |
| `price_excl` | number |  |
| `price_incl` | number |  |
| `product_id` | string |  |
| `sku` | string |  |
| `stock_level` | number |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/products/:product_id/variants` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-variants.md) for the provider-specific parameters and requirements.

