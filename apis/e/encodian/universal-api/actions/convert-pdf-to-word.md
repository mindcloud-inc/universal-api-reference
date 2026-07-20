# Encodian: Convert PDF To Word

Converts a PDF document to Word in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-pdf-to-word
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-pdf-to-word" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFilename": "Ava Chen",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-pdf-to-word', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFilename": "Ava Chen",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFilename` | string | yes | The output Microsoft Word filename including the file extension. |
| `fileContent` | string | yes | A Base64 encoded representation of the PDF file to be converted. |
| `conversionMode` | string | no | Select the conversion mode to use. Default: `Full`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognizeBullets` | boolean | no | Enable or disable the recognition of bullets. |

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
| `Errors` | array<string> | Any error messages returned by the operation. |
| `FileContent` | string | The processed Microsoft Word document content in Base64. |
| `Filename` | string | The filename of the Microsoft Word document. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Indicates whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Conversion/ConvertPdfToWord` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-word.md) for the provider-specific parameters and requirements.

