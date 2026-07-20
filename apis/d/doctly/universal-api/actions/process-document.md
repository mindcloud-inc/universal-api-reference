# Doctly: Process Document



```
POST https://connect.mindcloud.co/v1/universal/doctly/latest/actions/process-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doctly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/process-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doctly/latest/actions/process-document', {
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
| `file` | file | no | Document file to process. Provide either file or URL. |
| `url` | string | no | Public document URL to fetch and process. Provide either URL or file. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `accuracy` | string | no | Processing accuracy level: lite or ultra. Example: `ultra`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractorId` | string | no | Optional extractor UUID to use instead of standard Markdown conversion. Example: `987fcdeb-a654-3210-9876-543210987654`. |
| `pageSeparator` | boolean | no | Include page break markers in Markdown output. Default: `true`. |
| `skipImages` | boolean | no | Skip image extraction and transcription. Default: `false`. |
| `callbackUrl` | string | no | HTTPS webhook URL to notify when processing completes. Example: `https://example.com/webhooks/doctly`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "id": "string",
      "pageCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accuracy` | string |  |
| `createdAt` | date |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `id` | string |  |
| `pageCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Doctly API, this operation is `POST /documents` (base URL `https://api.doctly.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-document.md) for the provider-specific parameters and requirements.

