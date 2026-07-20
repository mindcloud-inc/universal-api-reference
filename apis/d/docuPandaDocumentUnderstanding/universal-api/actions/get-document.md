# DocuPanda - Document Understanding: Retrieve a Processed Document

Retrieves a processed document from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-document?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-document?${params}`, {
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
      "classIds": [
        "string"
      ],
      "classified": true,
      "dataset": "string",
      "documentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classIds` | array<string> | List of class IDs assigned to the document. If classified is False, this will be None. |
| `classified` | boolean | Whether the document has been classified. |
| `dataset` | string | Name of the dataset to which the document belongs. |
| `documentId` | string | Unique identifier of the document. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /document/:document_id` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

