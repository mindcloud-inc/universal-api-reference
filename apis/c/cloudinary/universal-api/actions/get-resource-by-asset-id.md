# Cloudinary: Get Resource by Asset ID

Retrieves a Cloudinary resource by asset ID.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-resource-by-asset-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-resource-by-asset-id?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-resource-by-asset-id?${params}`, {
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
| `assetId` | string | yes | The Cloudinary asset ID. |

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

Through the native Cloudinary API, this operation is `GET /resources/:asset_id` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-by-asset-id.md) for the provider-specific parameters and requirements.

