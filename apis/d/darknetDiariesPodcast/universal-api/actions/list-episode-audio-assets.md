# Darknet Diaries Podcast: List Episode Audio Assets

Retrieves episode audio assets from Darknet Diaries Podcast.

```
GET https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-episode-audio-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Darknet Diaries Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-episode-audio-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/list-episode-audio-assets?${params}`, {
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
      "episodeNumber": 1,
      "episodeTitle": "string",
      "guid": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "title": "string"
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
| `episodeNumber` | number |  |
| `episodeTitle` | string |  |
| `guid` | string |  |
| `publishedAt` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Darknet Diaries Podcast API, this operation is `GET /` (base URL `https://podcast.darknetdiaries.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episode-audio-assets.md) for the provider-specific parameters and requirements.

