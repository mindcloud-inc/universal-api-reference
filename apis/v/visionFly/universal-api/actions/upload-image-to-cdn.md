# VisionFly: Upload Image to CDN

Uploads an image to the VisionFly CDN.

```
POST https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/upload-image-to-cdn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/upload-image-to-cdn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/upload-image-to-cdn', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | Local file path or file input to upload to VisionFly. |
| `project` | string | no | Optional project slug to organize the uploaded image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "imageId": "string",
      "size": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Uploaded image MIME type. |
| `imageId` | string | Identifier of the uploaded image. |
| `size` | number | Uploaded image size in bytes. |
| `url` | string | Public VisionFly image URL. |

## Native endpoint

Through the native VisionFly API, this operation is `POST /cdn/upload` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image-to-cdn.md) for the provider-specific parameters and requirements.

