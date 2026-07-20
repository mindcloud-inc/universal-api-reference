# DocuPanda - Document Understanding: List Documents

Retrieves documents from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-documents?${params}`, {
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
| `dataset` | string | no | The dataset to filter documents by |
| `limit` | number | no | The maximum number of documents to return. Maximum is 1000 |
| `offset` | number | no | The number of documents to skip (to paginate through the dataset) |
| `exclude_payload` | boolean | no | Whether to exclude the result payload from the response |

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

Through the native DocuPanda - Document Understanding API, this operation is `GET /documents` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

