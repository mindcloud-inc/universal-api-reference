# Text to pdf: Upload File to ConvertAPI

Uploads a file to Text to PDF for later conversion.

```
POST https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/upload-file-to-convert-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Text to pdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/upload-file-to-convert-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/upload-file-to-convert-api', {
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
| `arguments` | object | no | Tool input arguments object. |
| `arguments.url` | string | no | Remote file URL to upload to ConvertAPI server. |
| `arguments.file` | file | no | MindCloud file object to upload to ConvertAPI server. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments.fileId` | string | no | Optional custom lowercase alphanumeric id for the uploaded file. |
| `arguments.filename` | string | no | Optional filename override for the uploaded file. |
| `arguments.headerName` | string | no | Optional header name for fetching a protected remote URL. |
| `arguments.headerValue` | string | no | Optional header value for fetching a protected remote URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "file_ext": "string",
        "file_id": "string",
        "file_name": "Ava Chen",
        "file_size": 1,
        "url": "https://example.com"
      },
      "error": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.file_ext` | string | Uploaded file extension. |
| `data.file_id` | string | Uploaded file id. |
| `data.file_name` | string | Uploaded file name. |
| `data.file_size` | number | Uploaded file size in bytes. |
| `data.url` | string | Temporary uploaded file URL. |
| `error` | string | Error message when execution fails. |
| `successful` | boolean | Whether the Composio tool execution succeeded. |

## Native endpoint

Through the native Text to pdf API, this operation is `POST /tools/execute/TEXT_TO_PDF_UPLOAD_FILE` (base URL `https://backend.composio.dev/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-to-convert-api.md) for the provider-specific parameters and requirements.

