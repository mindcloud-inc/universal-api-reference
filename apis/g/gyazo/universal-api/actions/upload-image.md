# Gyazo: Upload Image

Uploads a new image to Gyazo.

```
POST https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/upload-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gyazo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/upload-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imagedata": "Attach binary image content as multipart form data."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/upload-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imagedata": "Attach binary image content as multipart form data."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imagedata` | string | yes | Binary image data sent as multipart/form-data. Include a filename in the multipart part. Example: `Attach binary image content as multipart form data.`. |
| `accessPolicy` | string | no | Image visibility. Gyazo documents anyone or only_me. One of: `0`, `1`. Example: `anyone`. |
| `metadataIsPublic` | string | no | Whether page title and URL metadata should be public. One of: `0`, `1`. Example: `false`. |
| `refererUrl` | string | no | Referer site URL. Example: `https://example.com/page`. |
| `app` | string | no | Application name attached to the upload metadata. Example: `Chrome`. |
| `title` | string | no | Site title metadata. Example: `Home page`. |
| `desc` | string | no | Comment or description attached to the image. Example: `Screenshot of the home page`. |
| `createdAt` | number | no | Image creation time as a Unix timestamp. Example: `1715792342`. |
| `collectionId` | string | no | Collection identifier to add the image into. Example: `collection_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image_id": "string",
      "permalink_url": "https://example.com",
      "thumb_url": "https://example.com",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image_id` | string |  |
| `permalink_url` | string |  |
| `thumb_url` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Gyazo API, this operation is `POST https://upload.gyazo.com/api/upload` (base URL `https://api.gyazo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image.md) for the provider-specific parameters and requirements.

