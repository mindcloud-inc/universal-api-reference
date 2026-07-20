# Grok: Upload File in Chunks

Uploads file chunks to an existing Grok upload.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/upload-file-in-chunks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/upload-file-in-chunks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "chunk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/upload-file-in-chunks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "chunk": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | File identifier to upload chunks into. |
| `chunk` | string | yes | File data chunk payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Grok API returns.

## Native endpoint

Through the native Grok API, this operation is `POST /v1/files:uploadChunks` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-in-chunks.md) for the provider-specific parameters and requirements.

