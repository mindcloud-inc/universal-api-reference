# Vectara: Get Document

Retrieves a document from a specific Vectara corpus.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/get-document?connectionId=$CONNECTION_ID&corpusKey=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "corpusKey": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/get-document?${params}`, {
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
| `corpusKey` | string | yes | Unique key of the corpus. |
| `documentId` | string | yes | Unique ID of the document. |

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

Through the native Vectara API, this operation is `GET /v2/corpora/:corpus_key/documents/:document_id` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

