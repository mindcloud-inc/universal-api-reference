# DocuPipe: Standardize V3 (Beta)

Standardizes documents in DocuPipe using V3.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/standardize-v3-beta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/standardize-v3-beta" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "schemaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/standardize-v3-beta', {
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
| `schemaId` | string | yes | Schema to use for standardization (required for V3). |
| `guidelines` | string | no | Extraction guidelines. Overrides schema guidelines. |
| `useMetadata` | boolean | no | Whether to use metadata during standardization. Default: `false`. |
| `pages[]` | array<number> | no | Optional list of 0-indexed page numbers to standardize. If not provided, the entire document will be standardized. |
| `stdVersion` | list | no | Version of the standardization job. One of: `3`. |
| `effortLevel` | list | no | Level of effort for extraction. 'standard' uses cheaper/faster models (default), 'high' uses the best models. One of: `high`, `standard`. |
| `timeout` | number | no | The job timeout (in seconds) for webhook error reporting |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "jobId": "string",
      "pageCount": 1,
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
| `pageCount` | number | Number of pages being standardized. |
| `standardizationId` | string | Unique identifier of the standardization result. |
| `status` | string | Current status of the standardization job. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /v3/standardize` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/standardize-v3-beta.md) for the provider-specific parameters and requirements.

