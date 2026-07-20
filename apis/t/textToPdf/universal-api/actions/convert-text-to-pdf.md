# Text to pdf: Convert Text to PDF

Creates a PDF document from text in Text to PDF.

```
POST https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/convert-text-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Text to pdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/convert-text-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "arguments": {},
  "arguments.text": "string",
  "arguments.fileType": "txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/convert-text-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "arguments": {},
    "arguments.text": "string",
    "arguments.fileType": "txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments` | object | yes | Tool input arguments object. |
| `arguments.text` | string | yes | The complete plain text or Markdown content to convert to PDF. |
| `arguments.fileType` | list | yes | Input text format. Accepted values are txt and markdown. One of: `Markdown`, `Plain text`. Default: `txt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "file": {
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
| `data.file.mimetype` | string | Generated PDF MIME type. |
| `data.file.name` | string | Generated PDF file name. |
| `data.file.s3url` | string | Temporary downloadable URL for the generated PDF. |
| `error` | string | Error message when execution fails. |
| `successful` | boolean | Whether the Composio tool execution succeeded. |

## Native endpoint

Through the native Text to pdf API, this operation is `POST /tools/execute/TEXT_TO_PDF_CONVERT_TEXT_TO_PDF` (base URL `https://backend.composio.dev/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-pdf.md) for the provider-specific parameters and requirements.

