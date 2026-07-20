# DocuPanda - Document Understanding: List Standardizations

Retrieves standardizations from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-standardizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-standardizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-standardizations?${params}`, {
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
| `schema_id` | string | no | The schema ID to filter standardizations by |
| `document_id` | string | no | The ID of the document to filter standardizations by |
| `limit` | number | no | The maximum number of standardizations to return. Maximum is 1000 |
| `offset` | number | no | The number of standardizations to skip (to paginate through the data) |
| `exclude_payload` | boolean | no | Whether to exclude the data payload in the response |

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

Through the native DocuPanda - Document Understanding API, this operation is `GET /standardizations` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-standardizations.md) for the provider-specific parameters and requirements.

