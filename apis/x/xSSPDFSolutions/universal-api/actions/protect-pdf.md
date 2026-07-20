# XSS PDF Solutions: Protect PDF

Creates a protected PDF in XSS PDF Solutions.

```
POST https://connect.mindcloud.co/v1/universal/xSSPDFSolutions/latest/actions/protect-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XSS PDF Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xSSPDFSolutions/latest/actions/protect-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "Upload a PDF, or use the default sample PDF URL.",
  "userPass": "Password for the protected PDF."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xSSPDFSolutions/latest/actions/protect-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "Upload a PDF, or use the default sample PDF URL.",
    "userPass": "Password for the protected PDF."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The file to be protected with a password. Default: `https://raw.githubusercontent.com/ArturT/Test-PDF-Files/master/not_encrypted.pdf`. Example: `Upload a PDF, or use the default sample PDF URL.`. |
| `userPass` | string | yes | The password to lock the PDF. Default: `mindcloud-test`. Example: `Password for the protected PDF.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "output": {
        "data": {
          "result": "string"
        },
        "files": {
          "content": "string",
          "name": "Ava Chen",
          "path": "string"
        },
        "result": "string"
      },
      "status": "string",
      "steps": {
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Unique ID of the request. |
| `name` | string | The name of the operation. |
| `output.data.result` | string | Detailed operation result. |
| `output.files` | array<object> | Files returned by the operation. |
| `output.files.content` | string | Output file content when returned inline. |
| `output.files.name` | string | Name of the output file. |
| `output.files.path` | string | URL to access the output file. |
| `output.result` | string | Result message from the operation. |
| `status` | string | The current status of the process. |
| `steps` | array<object> | List of processing steps. |
| `steps.name` | string | Name of the processing step. |
| `steps.status` | string | Status of the processing step. |

## Native endpoint

Through the native XSS PDF Solutions API, this operation is `POST /api/32` (base URL `https://api.xss-cross-service-solutions.com/solutions/solutions`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/protect-pdf.md) for the provider-specific parameters and requirements.

