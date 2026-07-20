# SignalWire: List Documents

Retrieves documents from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "chunk_size": "string",
      "chunking_strategy": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "max_sentences_per_chunk": "string",
      "number_of_chunks": 1,
      "overlap_size": "string",
      "split_newlines": true,
      "status": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunk_size` | string | Chunk Size (only used for chunking type 'sliding') |
| `chunking_strategy` | string | Strategy used to chunk the document. |
| `created_at` | date | Document Creation Date. |
| `filename` | string | Name of the Document. |
| `id` | string | Unique ID of the Document. |
| `max_sentences_per_chunk` | string | Max Sentences per Chunk (only used for chunking type 'sentence') |
| `number_of_chunks` | number | Number of Chunks in the Document. |
| `overlap_size` | string | Overlap Size (only used for chunking type 'sliding') |
| `split_newlines` | boolean | Split on Newlines (only used for chunking type 'sentence') |
| `status` | string | Status of the Document. |
| `tags` | array<string> | Document tags. |
| `updated_at` | date | Document Update Date. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /datasphere/documents` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

