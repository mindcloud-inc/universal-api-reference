# TED Radio Hour Podcast: List Episodes

Retrieves episodes from the TED Radio Hour Podcast.

```
GET https://connect.mindcloud.co/v1/universal/tEDRadioHourPodcast/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TED Radio Hour Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tEDRadioHourPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tEDRadioHourPodcast/latest/actions/list-episodes?${params}`, {
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
      "audioLength": 1,
      "audioType": "string",
      "audioUrl": "https://example.com",
      "contentEncoded": "string",
      "description": "string",
      "duration": 1,
      "episodeType": "string",
      "explicit": "string",
      "guid": "string",
      "imageUrl": "https://example.com",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioLength` | number | Episode audio file length in bytes |
| `audioType` | string | Episode audio MIME type |
| `audioUrl` | string | Episode audio file URL |
| `contentEncoded` | string | Full encoded episode content |
| `description` | string | Episode description from the RSS feed |
| `duration` | number | Episode duration in seconds |
| `episodeType` | string | Episode type from the feed |
| `explicit` | string | Explicit-content flag from the feed |
| `guid` | string | Episode GUID |
| `imageUrl` | string | Episode image URL |
| `link` | string | Canonical NPR episode URL |
| `pubDate` | date | Episode publish date |
| `thumbnailUrl` | string | Episode thumbnail URL |
| `title` | string | Episode title |

## Native endpoint

Through the native TED Radio Hour Podcast API, this operation is `GET /510298/podcast.xml` (base URL `https://feeds.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

