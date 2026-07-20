# DocuPipe: Retrieve a Processed Document

Retrieves a processed document from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-processed-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-processed-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-processed-document?${params}`, {
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
| `documentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classIds": [
        "string"
      ],
      "classified": true,
      "dataset": "string",
      "documentId": "string",
      "fileExtension": "string",
      "filename": "Ava Chen",
      "fileType": "string",
      "language": "string",
      "metadata": {},
      "numPages": 1,
      "originalFileExtension": "string",
      "parentDocumentId": "string",
      "parentDocumentPages": [
        1
      ],
      "result": {},
      "status": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classIds` | array<string> | List of class IDs assigned to the document. If classified is False, this will be None. |
| `classified` | boolean | Whether the document has been classified. |
| `dataset` | string | Name of the dataset to which the document belongs. |
| `documentId` | string | Unique identifier of the document. |
| `fileExtension` | string | Extension of the document file. |
| `filename` | string | Name of the document file. |
| `fileType` | string | Type of the document file. |
| `language` | string | Dominant language of the document. |
| `metadata` | object | Metadata associated with the document. This is a user-defined dictionary that can have any properties. |
| `numPages` | number | Number of pages in the document. |
| `originalFileExtension` | string | extension of the originally uploaded file, before any conversion (e.g. html, docx). none if no conversion occurred. |
| `parentDocumentId` | string | Unique identifier of the parent document, if this document was created by splitting another document. |
| `parentDocumentPages` | array<number> | List of page numbers from the parent document that make up this document (zero indexed). |
| `result` | object | Result of the document analysis if completed. |
| `status` | string | Current status of the document processing (deprecated, will be removed in future versions). |
| `timestamp` | string | Timestamp of the document creation. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /document/:documentId` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-processed-document.md) for the provider-specific parameters and requirements.

