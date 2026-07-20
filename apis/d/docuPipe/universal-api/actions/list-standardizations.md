# DocuPipe: List Standardizations

Retrieves standardizations from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-standardizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-standardizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-standardizations?${params}`, {
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
| `schemaId` | string | no | The schema ID to filter standardizations by |
| `documentId` | string | no | The ID of the document to filter standardizations by |
| `excludePayload` | boolean | no | Whether to exclude the data payload in the response Default: `true`. |

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

Through the native DocuPipe API, this operation is `GET /standardizations` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-standardizations.md) for the provider-specific parameters and requirements.

