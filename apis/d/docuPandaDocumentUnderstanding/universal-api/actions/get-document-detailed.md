# DocuPanda - Document Understanding: Retrieve Detailed Processing Result

Retrieves detailed processing results from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-document-detailed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-document-detailed?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-document-detailed?${params}`, {
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
      "documentId": "string",
      "handwriting": true,
      "language": "string",
      "pages": [
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
| `documentId` | string | Unique identifier for the document |
| `handwriting` | boolean | True if the document contains handwriting |
| `language` | string | Language of the document, e.g. en, fr, etc. |
| `pages` | array<string> | List of parsed pages with detailed information on word level location |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /document/:document_id/detailed` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-detailed.md) for the provider-specific parameters and requirements.

