# Reka Vision: Update Video Metadata (V2)

Updates video metadata in Reka Vision.

```
PUT https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/update-video-metadata-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/update-video-metadata-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/update-video-metadata-v2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes |  |
| `title` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "features": {},
      "groupId": "string",
      "metadata": "string",
      "status": "string",
      "url": "https://example.com",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message if upload/download failed |
| `features` | object | Per-feature indexing statuses from the video_features table |
| `groupId` | string | Group ID if video belongs to a group |
| `metadata` | string | Metadata for a video |
| `status` | string | Upload status of the video |
| `url` | string | Presigned S3 URL to access the video |
| `videoId` | string | Unique identifier for the video |

## Native endpoint

Through the native Reka Vision API, this operation is `PATCH /v2/videos/:videoId` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video-metadata-v2.md) for the provider-specific parameters and requirements.

