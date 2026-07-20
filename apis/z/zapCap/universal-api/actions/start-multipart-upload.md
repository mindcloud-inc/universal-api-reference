# ZapCap: Start Multipart Upload

Starts a multipart video upload in ZapCap.

```
POST https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/start-multipart-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/start-multipart-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uploadParts[]": [
    "string"
  ],
  "filename": "tiny-sample.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/start-multipart-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uploadParts[]": ["string"],
    "filename": "tiny-sample.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadParts[]` | array | yes | Multipart part descriptors with contentLength values. |
| `filename` | string | yes | Filename to associate with the multipart upload session. Example: `tiny-sample.mp4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ZapCap API returns.

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/upload` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-multipart-upload.md) for the provider-specific parameters and requirements.

