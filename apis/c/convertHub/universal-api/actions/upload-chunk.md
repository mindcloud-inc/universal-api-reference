# ConvertHub: Upload Chunk

Uploads one file chunk to ConvertHub.

```
PUT https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/upload-chunk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/upload-chunk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "upload_987f6543-a21b-98c7-d654-321098765432",
  "chunkIndex": "0",
  "chunk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/upload-chunk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "upload_987f6543-a21b-98c7-d654-321098765432",
    "chunkIndex": "0",
    "chunk": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Example: `upload_987f6543-a21b-98c7-d654-321098765432`. |
| `chunkIndex` | number | yes | Example: `0`. |
| `chunk` | file | yes | The chunk data |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunk_index": 1,
      "session_id": "string",
      "success": true,
      "total_chunks": 1,
      "uploaded_chunks": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunk_index` | number |  |
| `session_id` | string |  |
| `success` | boolean |  |
| `total_chunks` | number |  |
| `uploaded_chunks` | number |  |

## Native endpoint

Through the native ConvertHub API, this operation is `POST /v2/upload/:sessionId/chunks/:chunkIndex` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-chunk.md) for the provider-specific parameters and requirements.

