# Hard Fork Podcast: List Episodes

Retrieves podcast episodes from Hard Fork Podcast.

```
GET https://connect.mindcloud.co/v1/universal/hardForkPodcast/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hard Fork Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hardForkPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hardForkPodcast/latest/actions/list-episodes?${params}`, {
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
      "author": "string",
      "content:encoded": {},
      "description": {},
      "enclosure": {},
      "guid": "string",
      "itunes:duration": "string",
      "itunes:episode": "string",
      "itunes:episodeType": "string",
      "itunes:explicit": "string",
      "itunes:subtitle": "string",
      "itunes:summary": "string",
      "link": "https://example.com",
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Episode author shown by the feed. |
| `content:encoded` | object | Full encoded episode content wrapper; rich HTML is stored under _cdata. |
| `description` | object | Episode description wrapper; rich HTML is stored under _cdata. |
| `enclosure` | object | Episode audio enclosure object from the feed. |
| `guid` | string | Unique episode identifier from the feed. |
| `itunes:duration` | string | Episode runtime from the iTunes metadata. |
| `itunes:episode` | string | Episode number when provided by the feed. |
| `itunes:episodeType` | string | Podcast episode type, for example full or trailer. |
| `itunes:explicit` | string | Whether the episode is marked explicit in the feed. |
| `itunes:subtitle` | string | Episode subtitle from the feed when available. |
| `itunes:summary` | string | Short episode summary from the feed. |
| `link` | string | Canonical Hard Fork page or episode page URL. |
| `pubDate` | string | Episode publication date in RSS format. |
| `title` | string | Episode title. |

## Native endpoint

Through the native Hard Fork Podcast API, this operation is `GET /6HKOhNgS` (base URL `https://feeds.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

