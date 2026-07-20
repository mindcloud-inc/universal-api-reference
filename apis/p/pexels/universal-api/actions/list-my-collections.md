# Pexels: List My Collections

Retrieves your saved collections from Pexels.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-my-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-my-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-my-collections?${params}`, {
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
      "collections": [
        {}
      ],
      "next_page": "string",
      "page": 1,
      "per_page": 1,
      "prev_page": "string",
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<object> | Collections for the authenticated Pexels account. |
| `next_page` | string | Next page URL when available. |
| `page` | number | Current page number. |
| `per_page` | number | Number of results returned per page. |
| `prev_page` | string | Previous page URL when available. |
| `total_results` | number | Total number of matching results. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/collections` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-my-collections.md) for the provider-specific parameters and requirements.

