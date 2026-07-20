# Darknet Diaries Podcast: List Recent Episodes

Retrieves recent podcast episodes from Darknet Diaries Podcast.

```
GET https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-recent-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Darknet Diaries Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-recent-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-recent-episodes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of recent episodes to return. Default: `10`. Example: `5`. |

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
| `audioLengthBytes` | number |  |
| `audioType` | string |  |
| `audioUrl` | string |  |
| `author` | string |  |
| `contentHtml` | string |  |
| `descriptionHtml` | string |  |
| `duration` | string |  |
| `episodeNumber` | number |  |
| `episodeTitle` | string |  |
| `episodeType` | string |  |
| `explicit` | boolean |  |
| `guid` | string |  |
| `imageUrl` | string |  |
| `link` | string |  |
| `publishedAt` | date |  |
| `seasonNumber` | number |  |
| `summary` | string |  |
| `title` | string |  |
| `transcriptType` | string |  |
| `transcriptUrl` | string |  |

## Native endpoint

Through the native Darknet Diaries Podcast API, this operation is `GET /` (base URL `https://podcast.darknetdiaries.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-episodes.md) for the provider-specific parameters and requirements.

