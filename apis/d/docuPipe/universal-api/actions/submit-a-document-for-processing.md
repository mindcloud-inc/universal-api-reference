# DocuPipe: Submit a Document for Processing

Submits a document for processing in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/submit-a-document-for-processing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/submit-a-document-for-processing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/submit-a-document-for-processing', {
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
| `document` | object | yes | The document to be analyzed, provided either as a file or via a URL. |
| `pages[]` | array<number> | no | List of page numbers to be parsed (zero indexed). If not provided, all pages will be parsed. |
| `dataset` | string | no | Name of the dataset to which you want to assign this document. It can be any string. This is useful to group your documents Default: `unassigned`. |
| `metadata` | object | no | Optional metadata to associate with the document. |
| `parseVersion` | number | no | Version of parsing. Available versions are 1, 2, 3 Default: `3`. |
| `processingMethod` | list | no | Method to use for processing the document. The options are: asImage (treats native PDFs as images), or removeWatermark (removes watermarks from PDFs before processing). Note that removeWatermark is experimental. One of: `asImage`, `removeWatermark`. |
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
| `status` | string | Current status of the document processing. |
| `workflowResponse` | object | *Advanced Feature* If you supplied a workfld In the input, the response will contain all the information to retrieve the outcome of the workflow. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /document` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-a-document-for-processing.md) for the provider-specific parameters and requirements.

