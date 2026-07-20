# FTrack: Complete Multipart Upload

Completes a multipart upload in FTrack.

```
POST https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/complete-multipart-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/complete-multipart-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "componentId": "string",
  "uploadId": "string",
  "parts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/complete-multipart-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "componentId": "string",
    "uploadId": "string",
    "parts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `componentId` | string | yes | Component identifier whose multipart upload should be completed. |
| `uploadId` | string | yes | Upload identifier returned by the upload metadata call. |
| `parts[]` | array<object> | yes | Uploaded multipart parts. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-multipart-upload.md) for the provider-specific parameters and requirements.

