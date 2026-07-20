# Yampi: List Product Reviews

Retrieves the reviews for a product in Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-product-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-product-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-product-reviews?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "id": 1,
      "rating": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `id` | number |  |
| `rating` | number |  |

## Native endpoint

Through the native Yampi API, this operation is `GET /:merchantAlias/catalog/products/:id/reviews` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-reviews.md) for the provider-specific parameters and requirements.

