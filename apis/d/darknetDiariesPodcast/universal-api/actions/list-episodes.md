# Darknet Diaries Podcast: List Episodes

Retrieves podcast episodes from Darknet Diaries Podcast.

```
GET https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Darknet Diaries Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-episodes?${params}`, {
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
      "seasonNumber": 1,
      "summary": "string",
      "title": "string",
      "transcriptType": "string",
      "transcriptUrl": "https://example.com"
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
| `episodeTitle` | string | Episode title without the prefixed number when available. |
| `episodeType` | string | iTunes episode type. |
| `explicit` | boolean | Whether the episode is marked explicit. |
| `guid` | string | Provider GUID for the episode. |
| `imageUrl` | string | Episode artwork URL. |
| `link` | string | Public Darknet Diaries episode page URL. |
| `publishedAt` | date | Episode publish timestamp in ISO 8601 format. |
| `seasonNumber` | number | Season number from iTunes metadata. |
| `summary` | string | Plain-text or lightly formatted episode summary. |
| `title` | string | Full episode title from the RSS feed. |
| `transcriptType` | string | Transcript MIME type when the feed provides one. |
| `transcriptUrl` | string | Transcript URL when the feed provides one. |

## Native endpoint

Through the native Darknet Diaries Podcast API, this operation is `GET /` (base URL `https://podcast.darknetdiaries.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

