# Zydon: List Sellers

Retrieves seller records from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-sellers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-sellers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-sellers?${params}`, {
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
      "currentPage": 1,
      "items": [
        {}
      ],
      "perPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number | Current page number. |
| `items` | array<object> | Sellers returned by Zydon. |
| `perPage` | number | Number of records per page. |
| `total` | number | Total number of records. |

## Native endpoint

Through the native Zydon API, this operation is `GET /sellers` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sellers.md) for the provider-specific parameters and requirements.

