# ConvertHub: Submit File for Conversion

Creates a file conversion job in ConvertHub.

```
POST https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/submit-file-for-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/submit-file-for-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "/absolute/path/to/source-file.pdf",
  "targetFormat": "pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/submit-file-for-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "/absolute/path/to/source-file.pdf",
    "targetFormat": "pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The file to convert (max 50MB for direct upload) Example: `/absolute/path/to/source-file.pdf`. |
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
      "metadata": {
        "user_ref": "string"
      },
      "result": {
        "download_url": "https://example.com",
        "expires_at": "string",
        "file_size": 1,
        "format": "string"
      },
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
| `metadata` | object |  |
| `metadata.user_ref` | string |  |
| `result` | object |  |
| `result.download_url` | string |  |
| `result.expires_at` | string |  |
| `result.file_size` | number |  |
| `result.format` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `POST /v2/convert` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-file-for-conversion.md) for the provider-specific parameters and requirements.

