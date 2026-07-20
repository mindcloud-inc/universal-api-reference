# DocuPanda - Document Understanding: Search Standardizations

Finds standardizations in DocuPanda by filename or IDs.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/search-standardizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/search-standardizations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/search-standardizations?${params}`, {
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
| `dataset` | string | no | Optional dataset filter |
| `limit` | number | no | Maximum number of results to return (1-500) |
| `offset` | number | no | Number of results to skip for pagination |
| `query` | string | yes | Search query to match against filename, document ID, or standardization ID |
| `schema_id` | string | no | Optional schema ID filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "documentId": "string",
      "schemaId": "string",
      "standardizationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The standardized result of the document. This is a structured JSON object. |
| `documentId` | string | Unique identifier of the document. |
| `schemaId` | string | Unique identifier of the schema used for standardization. |
| `standardizationId` | string | Unique identifier of the standardization object. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /standardizations/search` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-standardizations.md) for the provider-specific parameters and requirements.

