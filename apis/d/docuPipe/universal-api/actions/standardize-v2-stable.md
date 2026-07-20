# DocuPipe: Standardize V2 (Stable)

Standardizes documents in DocuPipe using V2.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/standardize-v2-stable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/standardize-v2-stable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/standardize-v2-stable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds[]` | array<string> | yes | List of document IDs to be standardized, up to 100 per batch. |
| `schemaId` | string | no | Unique identifier of the schema to be used for standardization - if not provided, one will be inferred. |
| `guidelines` | string | no | Guidelines to apply to the schema when standardizing. If this is provided, it will override the schema guidelines. |
| `useMetadata` | boolean | no | Whether to use metadata during standardization. Default: `false`. |
| `displayMode` | list | no | *Advanced Feature* Mode of display to run. The options are: `auto`: AI decides how to display the document (default) `spatial`: Display text spatially, as it appears in the document `sections`: Display text from top to bottom as sections, with tables appearing as markdown `image`: Display as an image, accompanied by section view One of: `auto`, `image`, `sections`, `spatial`. |
| `splitMode` | list | no | *Advanced Feature* Mode of splitting to run. Splitting is used to extract array fields efficiently. The options are: `auto`: AI decides how to split the document (default) `never`: Never split the document (this could lead to errors or poor performance for large documents) `all`: Split the document into individual pages One of: `all`, `auto`, `never`. |
| `effortLevel` | list | no | *Advanced Feature* Level of effort to run. The options are: `standard`: Standard effort level (default) `high`: High effort level, for more difficult documents One of: `extended`, `high`, `standard`. |
| `stdVersion` | list | no | Version of the standardization job. Options: 2.0, 2.1, 2.2 (default, stable), 2.3 (experimental, higher quality but may have runtime instability). One of: `2`, `2.1`, `2.2`, `2.3`. |
| `pages[]` | array<array> | no | *Advanced Feature* For every document, list of all pages that you want want to standardize. Page numbers are zero-indexed positions within each uploaded document. If not provided, the entire document will be standardized. |
| `timeout` | number | no | The job timeout (in seconds) for webhook error reporting |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "documentCount": 1,
      "jobId": "string",
      "pageCount": 1,
      "standardizationIds": [
        "string"
      ],
      "standardizationJobIds": [
        "string"
      ],
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string | Details of the status of the job. |
| `documentCount` | number | Number of documents this job will effect. Documents already standardized from previous runs will not be counted. |
| `jobId` | string | Unique identifier of the standardization job. |
| `pageCount` | number | Number of pages this job will effect. Pages already standardized from previous runs will not be counted. |
| `standardizationIds` | array<string> | List of individual standardization IDs that were created in this batch job. |
| `standardizationJobIds` | array<string> | List of individual standardization job IDs that were run in this batch job. |
| `status` | string | Current status of the standardization job. |
| `timestamp` | date | Timestamp of the last update to the job. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /v2/standardize/batch` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/standardize-v2-stable.md) for the provider-specific parameters and requirements.

