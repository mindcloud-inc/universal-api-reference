# fal.ai: Upload Local File

Creates a fal.ai storage file from a local upload.

```
POST https://connect.mindcloud.co/v1/universal/falai/latest/actions/upload-local-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/falai/latest/actions/upload-local-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetPath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/falai/latest/actions/upload-local-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetPath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetPath` | string | yes | Destination file path in fal.ai serverless storage. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native fal.ai API returns.

## Native endpoint

Through the native fal.ai API, this operation is `POST /serverless/files/file/local/:targetPath` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-local-file.md) for the provider-specific parameters and requirements.

