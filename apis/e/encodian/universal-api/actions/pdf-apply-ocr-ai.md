# Encodian: PDF Apply OCR AI

Applies OCR to a PDF in Encodian.

```
PUT https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-apply-ocr-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-apply-ocr-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-apply-ocr-ai', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | A Base64 encoded representation of the PDF file to be processed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "fileContent": "string",
      "filename": "Ava Chen",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by Encodian, if any. |
| `fileContent` | string | The Base64 encoded OCR PDF when available. |
| `filename` | string | The OCR PDF filename when available. |
| `httpStatusCode` | number | The HTTP status code returned by Encodian. |
| `httpStatusMessage` | string | The HTTP status message returned by Encodian. |
| `operationId` | string | The Encodian operation ID for the queued OCR operation. |
| `operationStatus` | string | The Encodian operation status. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/AIOcrPdfDocument` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-apply-ocr-ai.md) for the provider-specific parameters and requirements.

