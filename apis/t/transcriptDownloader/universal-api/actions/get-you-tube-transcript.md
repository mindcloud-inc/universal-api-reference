# Transcript Downloader: Get YouTube Transcript

Retrieves a YouTube transcript from Transcript Downloader.

```
GET https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-transcript?connectionId=$CONNECTION_ID&downloadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "downloadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-transcript?${params}`, {
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
| `downloadId` | string | yes | The transcript download ID returned by a create transcript action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download": {
        "cost": "string",
        "createdAt": "string",
        "id": "string",
        "mediaId": "string",
        "response": "string",
        "status": "string",
        "type": "string",
        "youtubeVideoId": "string"
      },
      "message": "string",
      "status": "string",
      "video": {
        "channelId": "string",
        "channelName": "Ava Chen",
        "channelUrl": "https://example.com",
        "commentCount": 1,
        "description": "string",
        "duration": "string",
        "likeCount": 1,
        "link": "https://example.com",
        "playlistName": "Ava Chen",
        "publishDateUTC": "string",
        "publishedAt": "string",
        "source": "string",
        "tags": [
          "string"
        ],
        "title": "string",
        "transcripts": "string",
        "transcriptsWithTimeStamps": [
          {
            "dur": "string",
            "start": "string",
            "text": "string"
          }
        ],
        "viewCount": 1,
        "youtubeId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download` | object |  |
| `download.cost` | string |  |
| `download.createdAt` | string |  |
| `download.id` | string |  |
| `download.mediaId` | string |  |
| `download.response` | string |  |
| `download.status` | string |  |
| `download.type` | string |  |
| `download.youtubeVideoId` | string |  |
| `message` | string |  |
| `status` | string |  |
| `video` | object |  |
| `video.channelId` | string |  |
| `video.channelName` | string |  |
| `video.channelUrl` | string |  |
| `video.commentCount` | number |  |
| `video.description` | string |  |
| `video.duration` | string |  |
| `video.likeCount` | number |  |
| `video.link` | string |  |
| `video.playlistName` | string |  |
| `video.publishDateUTC` | string |  |
| `video.publishedAt` | string |  |
| `video.source` | string |  |
| `video.tags` | array<string> |  |
| `video.title` | string |  |
| `video.transcripts` | string |  |
| `video.transcriptsWithTimeStamps` | array<object> |  |
| `video.transcriptsWithTimeStamps[].dur` | string |  |
| `video.transcriptsWithTimeStamps[].start` | string |  |
| `video.transcriptsWithTimeStamps[].text` | string |  |
| `video.viewCount` | number |  |
| `video.youtubeId` | string |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `GET /api/transcripts/:downloadId` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-you-tube-transcript.md) for the provider-specific parameters and requirements.

