# DocuPipe: Retrieve a Standardization XML

Retrieves standardization XML from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-standardization-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-standardization-xml?connectionId=$CONNECTION_ID&standardizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "standardizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-standardization-xml?${params}`, {
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
| `standardizationId` | string | yes |  |

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
      "timestamp": "string",
      "xml": "string"
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
| `xml` | string | The XML result of the standardization. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /standardization/:standardizationId/xml` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-standardization-xml.md) for the provider-specific parameters and requirements.

