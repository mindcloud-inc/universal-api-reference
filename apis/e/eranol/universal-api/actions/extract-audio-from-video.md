# Eranol: Extract Audio From Video

Creates an audio extraction job in Eranol.

```
POST https://connect.mindcloud.co/v1/universal/eranol/latest/actions/extract-audio-from-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eranol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/extract-audio-from-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eranol/latest/actions/extract-audio-from-video', {
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
| `url` | string | yes | Source video URL |
| `mono` | boolean | no | Extract mono audio when true |

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

Through the native Eranol API, this operation is `POST /ffmpeg/video/extract/audio` (base URL `https://eranol.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-audio-from-video.md) for the provider-specific parameters and requirements.

