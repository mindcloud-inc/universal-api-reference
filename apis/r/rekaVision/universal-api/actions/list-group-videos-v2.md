# Reka Vision: List Group Videos (V2)

Retrieves videos from a Reka Vision group.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/list-group-videos-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/list-group-videos-v2?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/list-group-videos-v2?${params}`, {
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
| `groupId` | string | yes |  |

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

Through the native Reka Vision API, this operation is `GET /v2/video-groups/:groupId/videos` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-videos-v2.md) for the provider-specific parameters and requirements.

