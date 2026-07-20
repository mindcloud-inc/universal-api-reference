# Colossyan: Retrieve Generated Video

Retrieves a generated video from Colossyan.

```
GET https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/retrieve-generated-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/retrieve-generated-video?connectionId=$CONNECTION_ID&videoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/retrieve-generated-video?${params}`, {
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
| `videoId` | string | yes | ID of the generated video to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "folderId": "string",
      "id": "string",
      "jobId": "string",
      "key": "string",
      "name": "Ava Chen",
      "publicUrl": "https://example.com",
      "shareId": "string",
      "thumbnailUrl": "https://example.com",
      "userId": "string",
      "videoDurationSeconds": 1,
      "videoSizeBytes": 1,
      "vttSubtitleString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | ISO timestamp when the generated video was created. |
| `folderId` | string | Folder ID containing the video when present. |
| `id` | string | Generated video ID. |
| `jobId` | string | Source video generation job ID. |
| `key` | string | Storage key for the generated video asset. |
| `name` | string | Generated video name. |
| `publicUrl` | string | Temporary Colossyan URL for downloading or previewing the video. |
| `shareId` | string | Share token for the generated video. |
| `thumbnailUrl` | string | Temporary Colossyan URL for the video thumbnail. |
| `userId` | string | Workspace user ID that owns the video. |
| `videoDurationSeconds` | number | Video duration in seconds. |
| `videoSizeBytes` | number | Video file size in bytes. |
| `vttSubtitleString` | string | WebVTT subtitle content for the generated video. |

## Native endpoint

Through the native Colossyan API, this operation is `GET /generated-videos/:videoId` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-generated-video.md) for the provider-specific parameters and requirements.

