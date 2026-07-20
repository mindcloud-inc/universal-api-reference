# DocuPanda - Document Understanding: Submit a Document for Processing

Creates a document processing request in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | object | yes |  |
| `pages` | list<number> | no | List of page numbers to be parsed (zero indexed). If not provided, all pages will be parsed. |
| `pages[]` | array<number> | no | List of page numbers to be parsed (zero indexed). If not provided, all pages will be parsed. |
| `dataset` | string | no | Name of the dataset to which you want to assign this document. It can be any string. This is useful to group your documents |
| `metadata` | object | no | Optional metadata to associate with the document. |
| `parseVersion` | number | no | Version of parsing. Available versions are 1, 2, 3 |
| `processingMethod` | string | no |  |
| `timeout` | number | no | The timeout in seconds for the job for webhook error reporting |
| `workflowId` | string | no | *Advanced Feature* Unique identifier of the workflow to be applied to the doucment once it is processed. See `POST /workflow/onSubmitDocument` for more details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "jobId": "string",
      "status": "string",
      "workflowResponse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | Unique identifier for the submitted document. |
| `jobId` | string | Unique identifier for the Document Upload Job. |
| `status` | string |  |
| `workflowResponse` | object |  |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /document` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-document.md) for the provider-specific parameters and requirements.

