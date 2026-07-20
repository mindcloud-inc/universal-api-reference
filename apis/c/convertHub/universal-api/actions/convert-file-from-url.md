# ConvertHub: Convert File from URL

Creates a file conversion job from a URL in ConvertHub.

```
POST https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/convert-file-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/convert-file-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://example.com/sample.pdf",
  "targetFormat": "pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/convert-file-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://example.com/sample.pdf",
    "targetFormat": "pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | URL of the file to convert (must be HTTP/HTTPS) Example: `https://example.com/sample.pdf`. |
| `targetFormat` | string | yes | Target format extension (e.g., "pdf", "jpg", "mp3") Example: `pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFilename` | string | no | Custom name for the output file Example: `converted-file.pdf`. |
| `webhookUrl` | string | no | URL to receive webhook notification when complete Example: `https://example.com/webhooks/converthub`. |
| `options` | object | no | Format-specific conversion options |
| `options.quality` | number | no | Quality setting (1-100) for lossy formats |
| `options.resolution` | string | no | Resolution for image/video conversions |
| `options.bitrate` | string | no | Bitrate for audio/video conversions |
| `options.sampleRate` | number | no | Sample rate for audio conversions |
| `metadata` | object | no | Custom metadata for tracking Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "estimated_time": "string",
      "job_id": "string",
      "links": {
        "cancel": "https://example.com",
        "status": "https://example.com"
      },
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimated_time` | string |  |
| `job_id` | string |  |
| `links` | object |  |
| `links.cancel` | string |  |
| `links.status` | string |  |
| `message` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `POST /v2/convert-url` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-file-from-url.md) for the provider-specific parameters and requirements.

