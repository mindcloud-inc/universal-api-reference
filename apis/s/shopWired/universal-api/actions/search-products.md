# ShopWired: Search products

Finds products in ShopWired by keyword.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/search-products?${params}`, {
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
| `keywords` | string | no | Keyword to search for. |
| `sessionId` | number | no | Used to make sure the search engine returns the same results in subsequent calls. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "price": 1,
      "sku": "string",
      "slug": "string",
      "stock": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `id` | number |  |
| `price` | number |  |
| `sku` | string |  |
| `slug` | string |  |
| `stock` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/search` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

