# WooCommerce: List Product Categories

Retrieves product categories from WooCommerce.

```
GET https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-product-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-product-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-product-categories?${params}`, {
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
| `search` | string | no | Limit results to those matching a string. |
| `slug` | string | no | Limit result set to resources with a specific slug. |
| `parentId` | list<number> | no | Limit result set to resources assigned to a specific parent. |
| `productId` | list<number> | no | Limit result set to resources assigned to a specific product. |
| `hideEmpty` | boolean | no | Whether to hide resources not assigned to any products. |

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

Through the native WooCommerce API, this operation is `GET /products/categories` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-categories.md) for the provider-specific parameters and requirements.

