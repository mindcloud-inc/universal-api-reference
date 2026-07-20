# Vectara: Upload File

Uploads a file to a Vectara corpus for indexing.

```
POST https://connect.mindcloud.co/v1/universal/vectara/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "corpusKey": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectara/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "corpusKey": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corpusKey` | string | yes | Unique key of the corpus. |
| `filename` | string | no | Optional override for the uploaded filename or document ID. |
| `file` | file | yes | Binary file to upload. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Metadata object to attach to the uploaded document. |
| `chunkingStrategy` | object | no | Chunking strategy for extracted text. |
| `tableExtractionConfig` | object | no | Table extraction configuration for supported files. |

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

Through the native Vectara API, this operation is `POST /v2/corpora/:corpus_key/upload_file` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

