# Encodian - Convert: Convert - PDF to PNG

Creates a PNG file from a PDF in Encodian - Convert.

```
POST https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-pdf-to-png
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-pdf-to-png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "bitDepth": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianConvert/latest/actions/convert-pdf-to-png', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "bitDepth": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | file | yes | The file content of the source PDF file. |
| `bitDepth` | number | yes | PDF bit depth for generated PNG output. |
| `outputFilename` | string | no | Output image filename. |

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

Through the native Encodian - Convert API, this operation is `POST /api/v1/Conversion/ConvertPdfToPng` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-png.md) for the provider-specific parameters and requirements.

