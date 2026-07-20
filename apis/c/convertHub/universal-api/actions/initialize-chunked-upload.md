# ConvertHub: Initialize Chunked Upload

Creates a chunked upload session in ConvertHub.

```
POST https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/initialize-chunked-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/initialize-chunked-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "sample.pdf",
  "fileSize": "1048576",
  "totalChunks": "2",
  "targetFormat": "pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/initialize-chunked-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "sample.pdf",
    "fileSize": "1048576",
    "totalChunks": "2",
    "targetFormat": "pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Original filename Example: `sample.pdf`. |
| `fileSize` | number | yes | Total file size in bytes Example: `1048576`. |
| `totalChunks` | number | yes | Number of chunks Example: `2`. |
| `targetFormat` | string | yes | Target format for conversion Example: `pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | no | URL to receive webhook notification when complete Example: `https://example.com/webhooks/converthub`. |
| `options` | object | no | Conversion options |
| `metadata` | object | no | Custom metadata Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "string",
      "links": {
        "complete": "https://example.com",
        "upload_chunk": "https://example.com"
      },
      "session_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | string |  |
| `links` | object |  |
| `links.complete` | string |  |
| `links.upload_chunk` | string |  |
| `session_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `POST /v2/upload/init` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-chunked-upload.md) for the provider-specific parameters and requirements.

