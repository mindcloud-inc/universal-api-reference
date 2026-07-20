# Nanonets OCR: Upload Document For Processing



```
POST https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/upload-document-for-processing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/upload-document-for-processing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "Select a workflow",
  "file": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/upload-document-for-processing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "Select a workflow",
    "file": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | list | yes | Workflow identifier. Example: `Select a workflow`. |
| `file` | file | yes | Document file to upload for processing. A public file URL can also be used for runtime testing via MindCloud's file handling. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `async` | boolean | no | Whether to process the document asynchronously. Default: `false`. |
| `metadata` | string | no | Optional metadata attached to the document. Use a JSON string when passing structured metadata. Example: `Example: {"source":"mindcloud-stage3","document_type":"invoice"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "metadata": "string",
      "originalDocumentName": "Ava Chen",
      "pages": [
        {
          "imageUrl": "https://example.com",
          "pageId": "string",
          "pageNumber": 1
        }
      ],
      "rawDocumentUrl": "https://example.com",
      "status": "string",
      "uploadedAt": "string",
      "verificationStage": "string",
      "verificationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string |  |
| `metadata` | string |  |
| `originalDocumentName` | string |  |
| `pages[].imageUrl` | string |  |
| `pages[].pageId` | string |  |
| `pages[].pageNumber` | number |  |
| `rawDocumentUrl` | string |  |
| `status` | string |  |
| `uploadedAt` | string |  |
| `verificationStage` | string |  |
| `verificationStatus` | string |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `POST /workflows/:workflow_id/documents` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-for-processing.md) for the provider-specific parameters and requirements.

