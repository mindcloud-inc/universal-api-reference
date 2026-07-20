# Voyage: Upload File

Uploads a file for Voyage batch processing.

```
POST https://connect.mindcloud.co/v1/universal/voyage/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "purpose": "batch"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voyage/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "purpose": "batch"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | JSONL file object to upload for batch processing. |
| `purpose` | list | yes | Purpose for the uploaded file. One of: `0`. Default: `batch`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "createdAt": "string",
      "expiresAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number | File size in bytes. |
| `createdAt` | string | File creation timestamp. |
| `expiresAt` | string | File expiration timestamp. |
| `filename` | string | Stored filename. |
| `id` | string | Voyage file ID. |
| `object` | string | Object type for the file. |
| `purpose` | string | Configured file purpose. |

## Native endpoint

Through the native Voyage API, this operation is `POST /v1/files` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

