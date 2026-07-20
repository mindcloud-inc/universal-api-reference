# Crime Junkie Podcast: List Comments

Retrieves comments from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-comments?${params}`, {
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
      "authorName": "Ava Chen",
      "authorUrl": "https://example.com",
      "content": {},
      "date": "2026-05-07T12:00:00.000Z",
      "dateGmt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
      "parent": 1,
      "post": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number |  |
| `authorName` | string |  |
| `authorUrl` | string |  |
| `content` | object |  |
| `date` | date |  |
| `dateGmt` | date |  |
| `id` | number |  |
| `link` | string |  |
| `parent` | number |  |
| `post` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /wp-json/wp/v2/comments` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

