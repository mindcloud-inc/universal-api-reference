# Printify: Upload Image

Uploads an image to Printify.

```
POST https://connect.mindcloud.co/v1/universal/printify/latest/actions/upload-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printify/latest/actions/upload-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "mindcloud-printify-test.png",
  "url": "https://png-pixel.com/1x1-ff00007f.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/upload-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "mindcloud-printify-test.png",
    "url": "https://png-pixel.com/1x1-ff00007f.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Name for the uploaded image file. Default: `mindcloud-printify-test.png`. |
| `url` | string | yes | Public URL for the image to upload. Default: `https://png-pixel.com/1x1-ff00007f.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "height": 1,
      "id": "string",
      "mimeType": "string",
      "previewUrl": "https://example.com",
      "uploadTime": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |
| `height` | number |  |
| `id` | string |  |
| `mimeType` | string |  |
| `previewUrl` | string |  |
| `uploadTime` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Printify API, this operation is `POST /uploads/images.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image.md) for the provider-specific parameters and requirements.

