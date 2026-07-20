# Platerecognizer: Upload Video For Stream Cloud

Uploads a video to Plate Recognizer Stream Cloud.

```
POST https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/upload-video-for-stream-cloud
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platerecognizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/upload-video-for-stream-cloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/upload-video-for-stream-cloud', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadUrl` | string | no | Public URL of the video to process in Stream Cloud. |
| `regions` | string | no | Comma-separated country or state codes to bias plate matching. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cameraId` | string | no | Unique camera identifier. |
| `mmc` | boolean | no | Set true to include make, model, orientation, and color when your license includes the add-on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cameraId": "string",
      "mmc": "string",
      "regions": [
        "string"
      ],
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cameraId` | string |  |
| `mmc` | string |  |
| `regions` | array<string> |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native Platerecognizer API, this operation is `POST /stream/video-upload/` (base URL `https://api.platerecognizer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-for-stream-cloud.md) for the provider-specific parameters and requirements.

