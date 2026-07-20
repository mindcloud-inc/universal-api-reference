# Text to pdf: Download File

Retrieves a file from Text to PDF by file ID.

```
GET https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Text to pdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/download-file?connectionId=$CONNECTION_ID&arguments=%5Bobject%20Object%5D&arguments.fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arguments": "[object Object]",
  "arguments.fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/download-file?${params}`, {
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
| `arguments` | object | yes | Tool input arguments object. |
| `arguments.fileId` | string | yes | Unique file id returned from upload or conversion. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments.download` | list | no | Download behavior: attachment or inline. One of: `Attachment`, `Inline`. Default: `attachment`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "content": {
          "mimetype": "string",
          "name": "Ava Chen",
          "s3url": "https://example.com"
        }
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
| `data.content.mimetype` | string | Downloaded file MIME type. |
| `data.content.name` | string | Downloaded file name. |
| `data.content.s3url` | string | Temporary downloadable file URL. |
| `error` | string | Error message when execution fails. |
| `successful` | boolean | Whether the Composio tool execution succeeded. |

## Native endpoint

Through the native Text to pdf API, this operation is `POST /tools/execute/TEXT_TO_PDF_DOWNLOAD_FILE` (base URL `https://backend.composio.dev/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

