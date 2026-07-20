# DocuPipe: Search Standardizations

Finds standardizations in DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/search-standardizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/search-standardizations?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/search-standardizations?${params}`, {
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
| `query` | string | yes | Search query to match against filename, document ID, or standardization ID |
| `schemaId` | string | no | Optional schema ID filter |
| `dataset` | string | no | Optional dataset filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "dataset": "string",
      "displayMode": "string",
      "documentId": "string",
      "fieldMetadata": {},
      "filename": "Ava Chen",
      "jobId": "string",
      "metadata": {},
      "pageMap": {},
      "schemaId": "string",
      "schemaName": "Ava Chen",
      "standardizationId": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The standardized result of the document. This is a structured JSON object. |
| `dataset` | string | Name of the dataset to which the document belongs |
| `displayMode` | string | Display mode actually used during standardization. |
| `documentId` | string | Unique identifier of the document. |
| `fieldMetadata` | object | Per-field extraction metadata mapping dot-paths to page numbers and confidence levels. |
| `filename` | string | Name of the file that was standardized. |
| `jobId` | string | Unique identifier of the job that created the standardization. |
| `metadata` | object | Metadata associated with the document that originated this standardization. This just echoes any metadata you have previously posted on document creation. |
| `pageMap` | object | Maps dot-paths to 1-indexed page numbers where each value was extracted from. |
| `schemaId` | string | Unique identifier of the schema used for standardization. |
| `schemaName` | string | Name of the schema used for standardization. |
| `standardizationId` | string | Unique identifier of the standardization object. |
| `timestamp` | string | Timestamp of the standardization job. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /standardizations/search` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-standardizations.md) for the provider-specific parameters and requirements.

