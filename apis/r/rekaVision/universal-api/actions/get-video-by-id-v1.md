# Reka Vision: Get Video By Id (V1)

Retrieves a video from Reka Vision by ID.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-video-by-id-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-video-by-id-v1?connectionId=$CONNECTION_ID&videoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-video-by-id-v1?${params}`, {
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
| `videoId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "indexingStatus": "string",
      "indexingType": "string",
      "metadata": "string",
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
| `groupId` | string | Group ID if video belongs to a group |
| `indexingStatus` | string | Status of video indexing |
| `indexingType` | string | Type of indexing applied to the video |
| `metadata` | string | Metadata for a video |
| `url` | string | Presigned S3 URL to access the video |
| `videoId` | string | Unique identifier for the video |

## Native endpoint

Through the native Reka Vision API, this operation is `GET /v1/videos/:videoId` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-by-id-v1.md) for the provider-specific parameters and requirements.

