# Fresh Air Podcast: List Episodes



```
GET https://connect.mindcloud.co/v1/universal/freshAirPodcast/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fresh Air Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshAirPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshAirPodcast/latest/actions/list-episodes?${params}`, {
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
      "content:encoded": {},
      "description": {},
      "enclosure": {},
      "guid": "string",
      "itunes:block": "string",
      "itunes:duration": "string",
      "itunes:episodeType": "string",
      "itunes:explicit": "string",
      "itunes:image": {},
      "itunes:title": "string",
      "link": "https://example.com",
      "media:thumbnail": {},
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
| `content:encoded` | object | Full encoded episode content wrapper; rich HTML is stored under _cdata. |
| `description` | object | Episode description wrapper; rich HTML is stored under _cdata. |
| `enclosure` | object | Episode audio enclosure object from the feed. |
| `guid` | string | Unique episode identifier from the NPR feed. |
| `itunes:block` | string | Whether the episode is blocked in the iTunes metadata. |
| `itunes:duration` | string | Episode runtime from the iTunes metadata. |
| `itunes:episodeType` | string | Podcast episode type, for example full. |
| `itunes:explicit` | string | Whether the episode is marked explicit. |
| `itunes:image` | object | Episode artwork object from the feed. |
| `itunes:title` | string | iTunes episode title. |
| `link` | string | Canonical NPR episode URL. |
| `media:thumbnail` | object | Episode thumbnail object when provided by the feed. |
| `pubDate` | string | Episode publication date in RSS format. |
| `title` | string | Episode title. |

## Native endpoint

Through the native Fresh Air Podcast API, this operation is `GET /381444908/podcast.xml` (base URL `https://feeds.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

