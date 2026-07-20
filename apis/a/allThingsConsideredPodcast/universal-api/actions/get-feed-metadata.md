# All Things Considered Podcast: Get Feed Metadata

Retrieves feed metadata from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-feed-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-feed-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-feed-metadata?${params}`, {
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
      "copyright": "string",
      "description": "string",
      "generator": "string",
      "imageLink": "https://example.com",
      "imageTitle": "string",
      "imageUrl": "https://example.com",
      "language": "string",
      "lastBuildDate": "string",
      "link": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `copyright` | string |  |
| `description` | string |  |
| `generator` | string |  |
| `imageLink` | string |  |
| `imageTitle` | string |  |
| `imageUrl` | string |  |
| `language` | string |  |
| `lastBuildDate` | string |  |
| `link` | string |  |
| `title` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET https://feeds.npr.org/2/rss.xml` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-metadata.md) for the provider-specific parameters and requirements.

