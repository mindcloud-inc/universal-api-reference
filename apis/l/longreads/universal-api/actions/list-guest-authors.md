# Longreads: List Guest Authors

Retrieves guest author profiles from Longreads.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-guest-authors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-guest-authors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-guest-authors?${params}`, {
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
      "author": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "featured_media": 1,
      "id": 1,
      "link": "https://example.com",
      "slug": "string",
      "title": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number |  |
| `date` | date |  |
| `featured_media` | number |  |
| `id` | number |  |
| `link` | string |  |
| `slug` | string |  |
| `title` | object |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/guest-author` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-guest-authors.md) for the provider-specific parameters and requirements.

