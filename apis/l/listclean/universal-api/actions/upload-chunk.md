# Listclean: Upload Chunk

Uploads a CSV chunk to Listclean.

```
PUT https://connect.mindcloud.co/v1/universal/listclean/latest/actions/upload-chunk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/upload-chunk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "upload_id": 1,
  "chunk_sequence_number": 1,
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listclean/latest/actions/upload-chunk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "upload_id": 1,
    "chunk_sequence_number": 1,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `upload_id` | number | yes | Upload ID returned by Start Upload. |
| `chunk_sequence_number` | number | yes | Sequence number for this chunk. |
| `content` | string | yes | Base64-encoded contents of the file chunk. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `md5_checksum` | string | no | Optional MD5 hash for file integrity checking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunk_details": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunk_details` | object | Chunk upload counts returned by Listclean. |

## Native endpoint

Through the native Listclean API, this operation is `POST /uploads/:upload_id` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-chunk.md) for the provider-specific parameters and requirements.

