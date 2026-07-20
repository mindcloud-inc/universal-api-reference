# Reka Vision: Upload Video (V2)

Uploads a video to Reka Vision without triggering indexing.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-video-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-video-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-video-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
| `videoName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | no |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": "string",
      "status": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | string | Video metadata (populated after upload completes) |
| `status` | string |  |
| `videoId` | string | Unique identifier for the uploaded video |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v2/videos` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-v2.md) for the provider-specific parameters and requirements.

