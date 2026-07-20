# Encodian: PDF Extract Text

Extracts text from a PDF in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-text?connectionId=$CONNECTION_ID&filename=sample.pdf&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "sample.pdf",
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-text?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | The PDF filename including the file extension Example: `sample.pdf`. |
| `fileContent` | string | yes | A Base64 encoded representation of the PDF file to be processed |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startPage` | number | no | Sets the page number to begin text extraction from |
| `endPage` | number | no | Sets the page number to end text extraction from |
| `removeControlCharacters` | boolean | no | Set whether control characters should be removed from the extracted text |
| `encodingType` | string | no | Sets the encoding type used for text extraction |
| `returnFile` | boolean | no | Set whether the action should return a file or alternatively an operation ID |

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
      "OperationStatus": "string",
      "TextLayer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Errors returned by Encodian, if any. |
| `FileContent` | string | The processed document content. |
| `Filename` | string | The filename of the document. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |
| `TextLayer` | string | The extracted text layer from the PDF document. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/GetPdfTextLayer` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/p-df-extract-text.md) for the provider-specific parameters and requirements.

