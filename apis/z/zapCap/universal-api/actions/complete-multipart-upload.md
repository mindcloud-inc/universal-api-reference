# ZapCap: Complete Multipart Upload

Completes a multipart video upload in ZapCap.

```
POST https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/complete-multipart-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/complete-multipart-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uploadId": "string",
  "videoId": "string",
  "parts[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/complete-multipart-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uploadId": "string",
    "videoId": "string",
    "parts[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadId` | string | yes | Multipart upload session ID returned by Start Multipart Upload. |
| `videoId` | string | yes | Video ID returned by Start Multipart Upload. |
| `parts[]` | array | yes | Uploaded multipart parts with etag and partNumber values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videoId` | string |  |

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/upload/complete` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-multipart-upload.md) for the provider-specific parameters and requirements.

