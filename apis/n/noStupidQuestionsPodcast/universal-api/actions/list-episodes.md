# No Stupid Questions Podcast: List Episodes

Retrieves podcast episodes from No Stupid Questions Podcast.

```
GET https://connect.mindcloud.co/v1/universal/noStupidQuestionsPodcast/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a No Stupid Questions Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noStupidQuestionsPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noStupidQuestionsPodcast/latest/actions/list-episodes?${params}`, {
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
      "audioLengthBytes": 1,
      "audioType": "string",
      "audioUrl": "https://example.com",
      "author": "string",
      "contentHtml": "string",
      "descriptionHtml": "string",
      "duration": "string",
      "episodeNumber": 1,
      "episodeTitle": "string",
      "episodeType": "string",
      "explicit": true,
      "guid": "string",
      "imageUrl": "https://example.com",
      "link": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z",
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
| `audioLengthBytes` | number | Audio file size in bytes when provided. |
| `audioType` | string | Audio MIME type. |
| `audioUrl` | string | Direct audio file URL. |
| `author` | string | Episode author. |
| `contentHtml` | string | Full encoded episode content HTML when present. |
| `descriptionHtml` | string | Episode description HTML from the RSS item description. |
| `duration` | string | Episode duration as published in the feed. |
| `episodeNumber` | number | Episode number from iTunes metadata. |
| `episodeTitle` | string | Episode title without the numeric prefix when available. |
| `episodeType` | string | iTunes episode type. |
| `explicit` | boolean | Whether the episode is marked explicit. |
| `guid` | string | Provider GUID for the episode. |
| `imageUrl` | string | Episode artwork URL when provided. |
| `link` | string | Public show or episode page URL from the RSS item. |
| `publishedAt` | date | Episode publish timestamp in ISO 8601 format. |
| `summary` | string | Plain-text episode summary. |
| `title` | string | Full episode title from the RSS feed. |

## Native endpoint

Through the native No Stupid Questions Podcast API, this operation is `GET` (base URL `https://feeds.simplecast.com/dfh_verV`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

