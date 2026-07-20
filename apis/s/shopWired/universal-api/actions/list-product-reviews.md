# ShopWired: List product reviews

Retrieves reviews for a product from ShopWired.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/list-product-reviews?${params}`, {
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
| `productId` | number | yes | The unique identifier of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "rating": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `rating` | number |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/{product_id}/reviews` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-reviews.md) for the provider-specific parameters and requirements.

