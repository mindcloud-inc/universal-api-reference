# Pixabay: Search Industry Images

Finds industry images in Pixabay.

```
GET https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-industry-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixabay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-industry-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-industry-images?${params}`, {
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
      "hits": [
        {}
      ],
      "total": 1,
      "totalHits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | array<object> | Image results returned by Pixabay. |
| `total` | number | Total number of matches for the query. |
| `totalHits` | number | Number of accessible results available through the API. |

## Native endpoint

Through the native Pixabay API, this operation is `GET /api/` (base URL `https://pixabay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-industry-images.md) for the provider-specific parameters and requirements.

