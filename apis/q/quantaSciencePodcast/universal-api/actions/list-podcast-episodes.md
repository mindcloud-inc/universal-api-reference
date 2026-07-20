# Quanta Science Podcast: List Podcast Episodes



```
GET https://connect.mindcloud.co/v1/universal/quantaSciencePodcast/latest/actions/list-podcast-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quanta Science Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantaSciencePodcast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantaSciencePodcast/latest/actions/list-podcast-episodes?${params}`, {
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
      "articleUrl": "https://example.com",
      "audioLength": 1,
      "audioType": "string",
      "audioUrl": "https://example.com",
      "author": "string",
      "description": "string",
      "descriptionHtml": "string",
      "duration": "string",
      "episodeType": "string",
      "guid": "string",
      "imageUrl": "https://example.com",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "season": 1,
      "source": "string",
      "subtitle": "string",
      "summary": "string",
      "summaryHtml": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articleUrl` | string | Quanta article URL extracted from the RSS description when present. |
| `audioLength` | number | Audio file length in bytes when present. |
| `audioType` | string | Audio MIME type from the RSS enclosure. |
| `audioUrl` | string | Direct tracked audio file URL from the RSS enclosure or media content. |
| `author` | string | Episode author/publisher. |
| `description` | string | Plain-text episode description derived from the RSS HTML description. |
| `descriptionHtml` | string | Original HTML description from the RSS item. |
| `duration` | string | Episode duration in the feed format. |
| `episodeType` | string | Podcast episode type, such as full. |
| `guid` | string | Stable RSS item identifier. |
| `imageUrl` | string | Episode artwork URL from the iTunes image field. |
| `link` | string | Podcast playback link from the RSS item. |
| `pubDate` | date | Episode publication date from the RSS item. |
| `season` | number | Podcast season number when present. |
| `source` | string | Static source label for the feed publisher. |
| `subtitle` | string | Short episode subtitle from the iTunes RSS field. |
| `summary` | string | Plain-text episode summary derived from the iTunes summary or RSS description. |
| `summaryHtml` | string | Original HTML summary from the RSS item. |
| `title` | string | Episode title. |

## Native endpoint

Through the native Quanta Science Podcast API, this operation is `GET /` (base URL `https://quantapodcast.quantamagazine.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-podcast-episodes.md) for the provider-specific parameters and requirements.

