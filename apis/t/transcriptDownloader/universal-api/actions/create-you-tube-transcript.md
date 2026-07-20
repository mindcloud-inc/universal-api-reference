# Transcript Downloader: Create YouTube Transcript

Creates a YouTube transcript in Transcript Downloader.

```
POST https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-you-tube-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-you-tube-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "youtubeVideoId": "string",
  "language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-you-tube-transcript', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "youtubeVideoId": "string",
    "language": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `youtubeVideoId` | string | yes | The YouTube video ID to transcribe. |
| `language` | string | yes | The transcript language code, such as en or de. |
| `includeComments` | boolean | no | Whether to include video comments in the response. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

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

Through the native Transcript Downloader API, this operation is `POST /api/transcripts` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-you-tube-transcript.md) for the provider-specific parameters and requirements.

