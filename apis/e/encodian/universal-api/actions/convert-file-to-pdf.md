# Encodian: Convert File To PDF

Converts a file to PDF in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-file-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-file-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "Base64 encoded file content",
  "outputFilename": "hello.pdf",
  "filename": "hello.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-file-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "Base64 encoded file content",
    "outputFilename": "hello.pdf",
    "filename": "hello.txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | A Base64 encoded representation of the file to be converted. Example: `Base64 encoded file content`. |
| `outputFilename` | string | yes | The filename to assign to the resulting PDF document. Example: `hello.pdf`. |
| `filename` | string | yes | The filename, including the file extension, of the file to be converted. Example: `hello.txt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `removeMarkup` | boolean | no | Sets whether comments and tracked changes should be removed from the document upon conversion. Default: `false`. Example: `false`. |
| `pdfACompliant` | boolean | no | Sets whether the resulting document should conform to PDF/A format. Default: `false`. Example: `false`. |
| `pdfAComplianceLevel` | string | no | Sets the required level of PDF/A compliance. Example: `1b`. |
| `generateBookmarks` | boolean | no | Set whether bookmarks should be automatically created for Microsoft Word documents that are converted to PDF. Default: `false`. Example: `false`. |
| `cultureName` | string | no | Set the culture for the documents prior to conversion. Example: `en-US`. |
| `returnFile` | boolean | no | Sets whether the action should return a file or, alternatively, an operation ID. Default: `true`. Example: `true`. |

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
| `errors[]` | string |  |
| `fileContent` | string |  |
| `filename` | string |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Conversion/BasicConversion` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-file-to-pdf.md) for the provider-specific parameters and requirements.

