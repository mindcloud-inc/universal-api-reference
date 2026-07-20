# All Things Considered Podcast: List Archive Shows

Retrieves archived shows from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-archive-shows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-archive-shows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-archive-shows?${params}`, {
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
      "affiliation": "string",
      "audioUrl": "https://example.com",
      "available": true,
      "duration": 1,
      "mediaId": "string",
      "program": "string",
      "slug": "string",
      "storyId": "string",
      "storyUrl": "https://example.com",
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliation` | string |  |
| `audioUrl` | string |  |
| `available` | boolean |  |
| `duration` | number |  |
| `mediaId` | string |  |
| `program` | string |  |
| `slug` | string |  |
| `storyId` | string |  |
| `storyUrl` | string |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET /programs/all-things-considered/archive` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-archive-shows.md) for the provider-specific parameters and requirements.

