# Lex Fridman Podcast: List Media

Retrieves media items from Lex Fridman Podcast.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/list-media?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/list-media?${params}`, {
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
      "dateGmt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
      "mediaType": "string",
      "mimeType": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "modifiedGmt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "sourceUrl": "https://example.com",
      "status": "string",
      "title": {},
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
| `date` | date |  |
| `dateGmt` | date |  |
| `id` | number |  |
| `link` | string |  |
| `mediaType` | string |  |
| `mimeType` | string |  |
| `modified` | date |  |
| `modifiedGmt` | date |  |
| `slug` | string |  |
| `sourceUrl` | string |  |
| `status` | string |  |
| `title` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/wp/v2/media` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

