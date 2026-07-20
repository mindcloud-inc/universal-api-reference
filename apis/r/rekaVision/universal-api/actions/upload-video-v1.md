# Reka Vision: Upload Video (V1)

Uploads a video to Reka Vision.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-video-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-video-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "index": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-video-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "index": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no |  |
| `videoUrl` | string | no |  |
| `index` | boolean | yes |  |
| `videoName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enableThumbnails` | boolean | no |  |
| `videoAbsoluteStartTimestamp` | string | no |  |
| `config` | string | no |  |
| `personIndexing` | boolean | no |  |
| `persistFrames` | boolean | no |  |
| `captionPrompt` | string | no |  |
| `encodeChunks` | boolean | no |  |
| `captionMode` | list<string> | no | One of: `generic`, `security`, `tagging_ad_video`, `tte_1110`. |
| `groupId` | string | no |  |
| `chunkingConfig` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "videoId": "string",
      "videoS3Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Status of the upload |
| `videoId` | string | Unique identifier for the uploaded video |
| `videoS3Url` | string | S3 URL of the uploaded video (null for background processing) |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v1/videos/upload` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-v1.md) for the provider-specific parameters and requirements.

