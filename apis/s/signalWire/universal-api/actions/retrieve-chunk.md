# SignalWire: Retrieve Chunk

Retrieves a chunk from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/retrieve-chunk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/retrieve-chunk?connectionId=$CONNECTION_ID&documentId=string&chunkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "chunkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/retrieve-chunk?${params}`, {
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
| `documentId` | string | yes | Unique ID of the parent Document. |
| `chunkId` | string | yes | Unique ID of a Chunk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "datasphere_document_id": "string",
      "id": "string",
      "project_id": "string",
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
| `content` | string | Content of the chunk |
| `created_at` | date | Chunk Creation Date. |
| `datasphere_document_id` | string | Unique ID of the chunk's datasphere document. |
| `id` | string | Unique ID of the chunk. |
| `project_id` | string | Unique ID of the project. |
| `status` | string | Status of the chunk. |
| `tags` | array<string> | The tags of the document associated with the chunk. |
| `updated_at` | date | Chunk Update Date. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /datasphere/documents/{documentId}/chunks/{chunkId}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-chunk.md) for the provider-specific parameters and requirements.

