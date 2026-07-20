# DocuPanda - Document Understanding: Standardize V2 (Stable)

Creates V2 standardizations in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-standardize-batch-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-standardize-batch-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds": "string",
  "documentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-standardize-batch-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds": "string",
    "documentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds` | list<string> | yes | List of document IDs to be standardized, up to 100 per batch. |
| `documentIds[]` | array<string> | yes | List of document IDs to be standardized, up to 100 per batch. |
| `pages` | list<object> | no | *Advanced Feature* For every document, list of all pages that you want want to standardize. Page numbers are zero-indexed positions within each uploaded document. If not provided, the entire document will be standardized. |
| `schemaId` | string | no | Unique identifier of the schema to be used for standardization - if not provided, one will be inferred. |
| `guidelines` | string | no | Guidelines to apply to the schema when standardizing. If this is provided, it will override the schema guidelines. |
| `useMetadata` | boolean | no | Whether to use metadata during standardization. |
| `displayMode` | string | no |  |
| `splitMode` | string | no |  |
| `effortLevel` | string | no |  |
| `stdVersion` | number | no |  |
| `pages[]` | array<string> | no | *Advanced Feature* For every document, list of all pages that you want want to standardize. Page numbers are zero-indexed positions within each uploaded document. If not provided, the entire document will be standardized. |
| `timeout` | number | no | The job timeout (in seconds) for webhook error reporting |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentCount": 1,
      "jobId": "string",
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
| `documentCount` | number | Number of documents this job will effect. Documents already standardized from previous runs will not be counted. |
| `jobId` | string | Unique identifier of the standardization job. |
| `status` | string |  |
| `timestamp` | string | Timestamp of the last update to the job. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /v2/standardize/batch` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-standardize-batch-v2.md) for the provider-specific parameters and requirements.

