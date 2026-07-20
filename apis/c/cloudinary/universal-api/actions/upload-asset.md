# Cloudinary: Upload Asset

Uploads an asset to your Cloudinary account.

```
POST https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/upload-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/upload-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "resourceType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/upload-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "resourceType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | The file to upload, a remote URL, or a data URI. |
| `resourceType` | string | yes | The Cloudinary resource type, such as image, video, or raw. |
| `publicId` | string | no | The identifier to assign to the uploaded asset. |
| `assetFolder` | string | no | The asset folder where the uploaded asset will be placed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset_folder": "string",
      "asset_id": "string",
      "bytes": 1,
      "created_at": "string",
      "display_name": "Ava Chen",
      "etag": "string",
      "format": "string",
      "height": 1,
      "original_filename": "Ava Chen",
      "placeholder": true,
      "public_id": "string",
      "resource_type": "string",
      "secure_url": "https://example.com",
      "signature": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "url": "https://example.com",
      "version": 1,
      "version_id": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset_folder` | string |  |
| `asset_id` | string |  |
| `bytes` | number |  |
| `created_at` | string |  |
| `display_name` | string |  |
| `etag` | string |  |
| `format` | string |  |
| `height` | number |  |
| `original_filename` | string |  |
| `placeholder` | boolean |  |
| `public_id` | string |  |
| `resource_type` | string |  |
| `secure_url` | string |  |
| `signature` | string |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `version` | number |  |
| `version_id` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Cloudinary API, this operation is `POST /:resource_type/upload` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-asset.md) for the provider-specific parameters and requirements.

