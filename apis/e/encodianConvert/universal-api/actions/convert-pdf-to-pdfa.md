# Encodian - Convert: Convert - PDF to PDFA

Creates a PDF/A file from a PDF in Encodian - Convert.

```
POST https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-pdf-to-pdfa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-pdf-to-pdfa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-pdf-to-pdfa', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | The filename of the source PDF file, including extension. |
| `fileContent` | file | no | PDF file content to convert. |
| `pdfaComplianceLevel` | string | no | Target PDF/A compliance level. |
| `finalOperation` | boolean | no | Whether to return the converted file content immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Errors returned by Encodian. |
| `FileContent` | string | Processed document content, usually Base64 encoded. |
| `Filename` | string | Filename of the processed document. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Convert API, this operation is `POST /api/v1/Conversion/ConvertToPdfA` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-pdfa.md) for the provider-specific parameters and requirements.

