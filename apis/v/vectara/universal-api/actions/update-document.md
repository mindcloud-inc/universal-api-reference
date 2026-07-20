# Vectara: Update Document

Updates an existing document in a specific Vectara corpus.

```
PUT https://connect.mindcloud.co/v1/universal/vectara/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "corpusKey": "string",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectara/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "corpusKey": "string",
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corpusKey` | string | yes | Unique key of the corpus. |
| `documentId` | string | yes | Unique ID of the document. |
| `metadata` | object | no | Document metadata fields to merge into the existing document metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extraction_usage": {},
      "id": "string",
      "images": [
        {}
      ],
      "metadata": {},
      "parts": [
        {}
      ],
      "storage_usage": {},
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extraction_usage` | object | Extraction usage consumed by the document. |
| `id` | string | The document ID. |
| `images` | array<object> | Images extracted from the document. |
| `metadata` | object | The document metadata. |
| `parts` | array<object> | Parts of the document. |
| `storage_usage` | object | Storage usage consumed by the document. |
| `tables` | array<object> | Tables extracted from the document. |

## Native endpoint

Through the native Vectara API, this operation is `PATCH /v2/corpora/:corpus_key/documents/:document_id` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

