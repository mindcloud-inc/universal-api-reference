# Creator Science Podcast: List Podcast Episodes

Retrieves podcast episodes from the Creator Science Podcast feed.

```
GET https://connect.mindcloud.co/v1/universal/creatorSciencePodcast/latest/actions/list-podcast-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creator Science Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatorSciencePodcast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/creatorSciencePodcast/latest/actions/list-podcast-episodes?${params}`, {
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
      "audioType": "string",
      "audioUrl": "https://example.com",
      "author": "Ava Chen",
      "contentHtml": "string",
      "description": "string",
      "durationSeconds": 1,
      "episodeNumber": 1,
      "episodeType": "string",
      "guid": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "isExplicit": true,
      "link": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "rawTitle": "string",
      "seasonNumber": 1,
      "subtitle": "string",
      "summary": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioType` | string | MIME type for the audio enclosure. |
| `audioUrl` | string | Audio enclosure URL for the episode. |
| `author` | string | Episode author. |
| `contentHtml` | string | Full HTML show notes from content:encoded. |
| `description` | string | RSS description text for the episode. |
| `durationSeconds` | number | Episode duration in seconds. |
| `episodeNumber` | number | Episode number when provided by the feed. |
| `episodeType` | string | RSS episode type, such as full or trailer. |
| `guid` | string | RSS guid value for the episode. |
| `id` | string | Stable episode identifier from the RSS guid, link, or title. |
| `imageUrl` | string | Episode artwork URL when provided. |
| `isExplicit` | boolean | Whether the episode is marked explicit in the feed. |
| `link` | string | Public episode page URL. |
| `publishedAt` | date | Episode publication date from pubDate. |
| `rawTitle` | string | Original RSS title value including any feed numbering. |
| `seasonNumber` | number | Season number when provided by the feed. |
| `subtitle` | string | Short episode subtitle from the iTunes RSS namespace. |
| `summary` | string | Episode summary text. |
| `title` | string | Episode title. |

## Native endpoint

Through the native Creator Science Podcast API, this operation is `GET /TPG4024225475` (base URL `https://feeds.megaphone.fm`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-podcast-episodes.md) for the provider-specific parameters and requirements.

