# Encodian: PDF Merge Files

Merges PDF files in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-merge-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-merge-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFilename": "merged.pdf",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-merge-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFilename": "merged.pdf",
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFilename` | string | yes | The filename to assign to the resulting PDF document including extension. Example: `merged.pdf`. |
| `documents[]` | array<object> | yes | JSON array containing a filename and base64 document content for each document to merge. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generateBookmarks` | boolean | no | Generate a bookmark for each merged PDF document. |
| `pageNormalisation` | boolean | no | Normalise page width and height to the dimensions of the first file. |
| `preserveBookmarks` | boolean | no | Preserve bookmarks contained within each merged PDF document. |
| `removeMarkup` | boolean | no | Remove comments and tracked changes from Microsoft Office documents on conversion. |
| `pdfACompliant` | boolean | no | Set whether the resulting document should conform to PDF/A format. |
| `pdfAComplianceLevel` | string | no | Set the required level of PDF/A compliance. Example: `PDF_A_2A`. |
| `returnFile` | boolean | no | Set whether the action returns a file or an operation ID. Default: `true`. |

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
| `fileContent` | string | The Base64 encoded merged PDF when available. |
| `filename` | string | The merged PDF filename when available. |
| `httpStatusCode` | number | The HTTP status code returned by Encodian. |
| `httpStatusMessage` | string | The HTTP status message returned by Encodian. |
| `operationId` | string | The Encodian operation ID for the queued merge. |
| `operationStatus` | string | The Encodian operation status. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/MergeArrayOfDocumentsToPdf` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-merge-files.md) for the provider-specific parameters and requirements.

