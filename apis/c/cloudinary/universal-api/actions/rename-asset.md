# Cloudinary: Rename Asset

Renames an asset in your Cloudinary account.

```
PUT https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/rename-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/rename-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromPublicId": "string",
  "resourceType": "string",
  "toPublicId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/rename-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromPublicId": "string",
    "resourceType": "string",
    "toPublicId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromPublicId` | string | yes | The current public ID. |
| `resourceType` | string | yes | The Cloudinary resource type, such as image, video, or raw. |
| `toPublicId` | string | yes | The new public ID. |

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
      "format": "string",
      "height": 1,
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
| `format` | string |  |
| `height` | number |  |
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

Through the native Cloudinary API, this operation is `POST /:resource_type/rename` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-asset.md) for the provider-specific parameters and requirements.

