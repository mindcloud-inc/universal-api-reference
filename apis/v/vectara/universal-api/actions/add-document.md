# Vectara: Add Document

Adds a document to a Vectara corpus for indexing.

```
POST https://connect.mindcloud.co/v1/universal/vectara/latest/actions/add-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/add-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "corpusKey": "string",
  "type": "0",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectara/latest/actions/add-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "corpusKey": "string",
    "type": "0",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corpusKey` | string | yes | Unique key of the corpus. |
| `waitFor` | list | no | Wait until the document is searchable or fully indexed before returning. One of: `0`, `1`. |
| `type` | list | yes | Document payload type. One of: `0`, `1`. |
| `id` | string | yes | Unique document ID within the corpus. |
| `title` | string | no | Document title for structured documents. |
| `description` | string | no | Document description for structured documents. |
| `metadata` | object | no | Document-level metadata object. |
| `sections[]` | array<object> | no | Structured document sections array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentParts[]` | array<object> | no | Core document parts array. |
| `customDimensions` | object | no | Document-level custom dimensions. |
| `chunkingStrategy` | object | no | Optional chunking strategy for structured documents. |

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

Through the native Vectara API, this operation is `POST /v2/corpora/:corpus_key/documents` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-document.md) for the provider-specific parameters and requirements.

