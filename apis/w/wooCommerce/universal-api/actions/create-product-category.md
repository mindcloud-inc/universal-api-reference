# WooCommerce: Create Product Category

Creates a new product category in WooCommerce.

```
POST https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-product-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-product-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-product-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Category name. |
| `slug` | string | no | Category slug. |
| `description` | string | no | Category description. |
| `parent` | list<number> | no | Numeric ID of the parent category. |
| `display` | list<string> | no | One of: `both`, `default`, `products`, `subcategories`. |
| `image` | object | no |  |
| `image.id` | number | no |  |
| `image.src` | string | no |  |
| `image.name` | string | no |  |
| `image.alt` | string | no |  |
| `menuOrder` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "description": "string",
      "display": "string",
      "id": 1,
      "menuOrder": 1,
      "name": "Ava Chen",
      "parent": 1,
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `description` | string |  |
| `display` | string |  |
| `id` | number |  |
| `menuOrder` | number |  |
| `name` | string |  |
| `parent` | number |  |
| `slug` | string |  |

## Native endpoint

Through the native WooCommerce API, this operation is `POST /products/categories` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-category.md) for the provider-specific parameters and requirements.

