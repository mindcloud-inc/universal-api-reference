# DocuPanda - Document Understanding: Analyze Document

Creates a document analysis in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-analyze-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-analyze-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "questions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-analyze-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "questions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Unique identifier of the document to be questioned. |
| `instructions` | string | no | Global instructions to provide additional guidelines or context to the AI when answering the questions. |
| `pages` | list<number> | no | List of page numbers to be analyzed (zero indexed). If not provided, all pages will be analyzed. |
| `questions` | list<string> | yes | List of questions to be answered. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisId": "string",
      "jobId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisId` | string | Unique identifier for the analysis. |
| `jobId` | string | Unique identifier for the submitted job. |
| `success` | boolean | Whether the job was successful launched or not. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /analyze/document` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-analyze-document.md) for the provider-specific parameters and requirements.

