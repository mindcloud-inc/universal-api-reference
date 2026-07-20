# Transcript Downloader: Initialize YouTube Audio Download

Creates a YouTube audio download in Transcript Downloader.

```
POST https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/initialize-you-tube-audio-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/initialize-you-tube-audio-download" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "youtubeVideoId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/initialize-you-tube-audio-download', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "youtubeVideoId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `youtubeVideoId` | string | yes | The YouTube video ID to process. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com",
      "cost": "string",
      "createdAt": "string",
      "duration": "string",
      "fileUrls": [
        "https://example.com"
      ],
      "id": "string",
      "mediaId": "string",
      "status": "string",
      "transcriptSpeakerCost": "string",
      "transcriptSpeakerId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string |  |
| `cost` | string |  |
| `createdAt` | string |  |
| `duration` | string |  |
| `fileUrls` | array<string> |  |
| `id` | string |  |
| `mediaId` | string |  |
| `status` | string |  |
| `transcriptSpeakerCost` | string |  |
| `transcriptSpeakerId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/downloads/audio` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-you-tube-audio-download.md) for the provider-specific parameters and requirements.

