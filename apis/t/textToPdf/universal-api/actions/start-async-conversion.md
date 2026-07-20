# Text to pdf: Start Async Conversion

Starts an asynchronous file conversion job in Text to PDF.

```
POST https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/start-async-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Text to pdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/start-async-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "arguments": {},
  "arguments.fromFormat": "string",
  "arguments.toFormat": "pdf",
  "arguments.file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/start-async-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "arguments": {},
    "arguments.fromFormat": "string",
    "arguments.toFormat": "pdf",
    "arguments.file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments` | object | yes | Tool input arguments object. |
| `arguments.fromFormat` | string | yes | Source file format, such as txt, docx, or html. |
| `arguments.toFormat` | string | yes | Target output format, such as pdf. Default: `pdf`. |
| `arguments.file` | string | yes | Public file URL or file content to convert. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments.jobId` | string | no | Optional custom 32-character lowercase alphanumeric job id. |
| `arguments.webhook` | string | no | Optional callback URL for conversion completion notification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "job_id": "string"
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
| `data.job_id` | string | Asynchronous conversion job id. |
| `error` | string | Error message when execution fails. |
| `successful` | boolean | Whether the Composio tool execution succeeded. |

## Native endpoint

Through the native Text to pdf API, this operation is `POST /tools/execute/TEXT_TO_PDF_START_ASYNC_CONVERSION` (base URL `https://backend.composio.dev/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-async-conversion.md) for the provider-specific parameters and requirements.

