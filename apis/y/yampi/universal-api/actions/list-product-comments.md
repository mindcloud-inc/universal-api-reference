# Yampi: List Product Comments

Retrieves a list of product comments from Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-product-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-product-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-product-comments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "id": 1,
      "product_id": 1
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
| `product_id` | number |  |

## Native endpoint

Through the native Yampi API, this operation is `GET /:merchantAlias/catalog/comments` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-comments.md) for the provider-specific parameters and requirements.

