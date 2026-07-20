# DocuPanda - Document Understanding: Split a Document

Creates split documents from a DocuPanda document.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-split-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-split-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-split-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataset` | string | no | Dataset to assign to the newly generated documents. |
| `displayMode` | string | no |  |
| `documentId` | string | yes | Unique identifier of the document to be split. |
| `filenamePrefix` | string | no | Prefix to use for the filenames of the newly generated documents. |
| `instructions` | string | no | Instructions for how the splitting should be done (optional). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "success": true,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique identifier for the submitted job. |
| `success` | boolean | Whether the job was successfully submitted. |
| `timestamp` | string | Timestamp of when the job was submitted. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /document/split` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-split-document.md) for the provider-specific parameters and requirements.

