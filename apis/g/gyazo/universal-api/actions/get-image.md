# Gyazo: Get Image

Retrieves an image from Gyazo.

```
GET https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gyazo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-image?connectionId=$CONNECTION_ID&imageId=8980c52421e452ac3355ca3e5cfe7a0c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "8980c52421e452ac3355ca3e5cfe7a0c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-image?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageId` | string | yes | The Gyazo image ID. Example: `8980c52421e452ac3355ca3e5cfe7a0c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "image_id": "string",
      "metadata": {},
      "ocr": {},
      "permalink_url": "https://example.com",
      "thumb_url": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `image_id` | string |  |
| `metadata` | object |  |
| `ocr` | object |  |
| `permalink_url` | string |  |
| `thumb_url` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Gyazo API, this operation is `GET /api/images/:image_id` (base URL `https://api.gyazo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image.md) for the provider-specific parameters and requirements.

