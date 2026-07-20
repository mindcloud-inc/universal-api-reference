# DocuPanda - Document Understanding: Retrieve a Standardization XML

Retrieves a standardization XML result from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-standardization-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-standardization-xml?connectionId=$CONNECTION_ID&standardization_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "standardization_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-standardization-xml?${params}`, {
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
| `standardization_id` | string | yes |  |

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

Through the native DocuPanda - Document Understanding API, this operation is `GET /standardization/:standardization_id/xml` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-standardization-xml.md) for the provider-specific parameters and requirements.

