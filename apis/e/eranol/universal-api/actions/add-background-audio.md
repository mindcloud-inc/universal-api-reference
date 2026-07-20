# Eranol: Add Background Audio

Creates a background audio job in Eranol.

```
POST https://connect.mindcloud.co/v1/universal/eranol/latest/actions/add-background-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eranol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/add-background-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video_url": "https://example.com",
  "bg_audio_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eranol/latest/actions/add-background-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video_url": "https://example.com",
    "bg_audio_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video_url` | string | yes | Source video URL |
| `bg_audio_url` | string | yes | Background audio file URL |
| `bg_audio_volume` | number | no | Background audio mix volume |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "jobType": "string",
      "message": "string",
      "resultUrl": "https://example.com",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Created job identifier |
| `jobType` | string | Eranol job type |
| `message` | string | Provider status message |
| `resultUrl` | string | Result retrieval URL |
| `status` | string | Initial job status |
| `statusUrl` | string | Status polling URL |

## Native endpoint

Through the native Eranol API, this operation is `POST /ffmpeg/video/add-bg-audio` (base URL `https://eranol.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-background-audio.md) for the provider-specific parameters and requirements.

