# Transcript Downloader: Initialize Instagram Audio Download

Creates an Instagram audio download in Transcript Downloader.

```
POST https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/initialize-instagram-audio-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/initialize-instagram-audio-download" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/initialize-instagram-audio-download', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The Instagram post or reel URL. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com",
      "cost": "string",
      "downloadId": "string",
      "duration": "string",
      "fileUrls": [
        "https://example.com"
      ],
      "id": "string",
      "mediaId": "string",
      "message": "string",
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
| `downloadId` | string |  |
| `duration` | string |  |
| `fileUrls` | array<string> |  |
| `id` | string |  |
| `mediaId` | string |  |
| `message` | string |  |
| `status` | string |  |
| `transcriptSpeakerCost` | string |  |
| `transcriptSpeakerId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/instagram/audio` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-instagram-audio-download.md) for the provider-specific parameters and requirements.

