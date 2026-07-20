# Transcript Downloader: Get Download

Retrieves a download from Transcript Downloader.

```
GET https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-download?connectionId=$CONNECTION_ID&downloadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "downloadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-download?${params}`, {
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
| `downloadId` | string | yes | The download ID returned by a Transcript Downloader create action. |

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

Through the native Transcript Downloader API, this operation is `GET /downloads/:downloadId` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-download.md) for the provider-specific parameters and requirements.

