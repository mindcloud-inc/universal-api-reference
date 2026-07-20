# Modelry: Create Blob



```
POST https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-blob
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modelry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-blob" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blob.filename": "Ava Chen",
  "blob.byteSize": 1,
  "blob.checksum": "string",
  "blob.contentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-blob', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blob.filename": "Ava Chen",
    "blob.byteSize": 1,
    "blob.checksum": "string",
    "blob.contentType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blob.filename` | string | yes | Filename for the blob. |
| `blob.byteSize` | number | yes | File size in bytes. |
| `blob.checksum` | string | yes | Base64-encoded MD5 checksum. |
| `blob.contentType` | string | yes | File content type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Modelry API returns.

## Native endpoint

Through the native Modelry API, this operation is `POST /v1/blobs` (base URL `https://api.modelry.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blob.md) for the provider-specific parameters and requirements.

