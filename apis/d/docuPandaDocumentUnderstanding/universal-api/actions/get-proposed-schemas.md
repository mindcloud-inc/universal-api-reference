# DocuPanda - Document Understanding: Get Schema Proposals

Retrieves schema proposals for a document from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-proposed-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-proposed-schemas?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-proposed-schemas?${params}`, {
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
| `document_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentDescription": "string",
      "schemas": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentDescription` | string |  |
| `schemas` | array<string> |  |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /document/:document_id/proposed-schemas` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proposed-schemas.md) for the provider-specific parameters and requirements.

