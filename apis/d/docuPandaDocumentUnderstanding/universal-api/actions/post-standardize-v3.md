# DocuPanda - Document Understanding: Standardize V3 (Beta)

Creates V3 standardizations in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-standardize-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-standardize-v3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "schemaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-standardize-v3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "schemaId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Unique identifier of the document to be standardized. |
| `pages` | list<number> | no | Optional list of 0-indexed page numbers to standardize. If not provided, the entire document will be standardized. |
| `schemaId` | string | yes | Schema to use for standardization (required for V3). |
| `guidelines` | string | no | Extraction guidelines. Overrides schema guidelines. |
| `useMetadata` | boolean | no | Whether to use metadata during standardization. |
| `pages[]` | array<number> | no | Optional list of 0-indexed page numbers to standardize. If not provided, the entire document will be standardized. |
| `stdVersion` | number | no |  |
| `effortLevel` | string | no |  |
| `timeout` | number | no | The job timeout (in seconds) for webhook error reporting |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "jobId": "string",
      "standardizationId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | Document being standardized. |
| `jobId` | string | Unique identifier of the standardization job. |
| `standardizationId` | string | Unique identifier of the standardization result. |
| `status` | string |  |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /v3/standardize` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-standardize-v3.md) for the provider-specific parameters and requirements.

