# Cloudinary: Update Resource Details

Updates resource details in your Cloudinary account.

```
PUT https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/update-resource-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/update-resource-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/update-resource-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetId` | string | yes | The Cloudinary asset ID. |
| `displayName` | string | no | A user-friendly display name for the asset. |

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
      "last_updated": {},
      "public_id": "string",
      "resource_type": "string",
      "secure_url": "https://example.com",
      "tags": [
        "string"
      ],
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
| `display_name` | string |  |
| `format` | string |  |
| `height` | number |  |
| `last_updated` | object |  |
| `public_id` | string |  |
| `resource_type` | string |  |
| `secure_url` | string |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `version` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Cloudinary API, this operation is `PUT /resources/:asset_id` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource-details.md) for the provider-specific parameters and requirements.

