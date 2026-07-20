# Cloudinary: Get Resource by Public ID

Retrieves a Cloudinary resource by public ID.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-resource-by-public-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-resource-by-public-id?connectionId=$CONNECTION_ID&publicId=string&resourceType=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "resourceType": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-resource-by-public-id?${params}`, {
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
| `publicId` | string | yes | The Cloudinary public ID. |
| `resourceType` | string | yes | The Cloudinary resource type, such as image, video, or raw. |
| `type` | string | yes | The delivery type, such as upload, private, or authenticated. |

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
      "derived": [
        {}
      ],
      "display_name": "Ava Chen",
      "format": "string",
      "height": 1,
      "next_cursor": "string",
      "public_id": "string",
      "resource_type": "string",
      "secure_url": "https://example.com",
      "type": "string",
      "url": "https://example.com",
      "version": 1,
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
| `derived` | array<object> |  |
| `display_name` | string |  |
| `format` | string |  |
| `height` | number |  |
| `next_cursor` | string |  |
| `public_id` | string |  |
| `resource_type` | string |  |
| `secure_url` | string |  |
| `type` | string |  |
| `url` | string |  |
| `version` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /resources/:resource_type/:type/:public_id` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-by-public-id.md) for the provider-specific parameters and requirements.

