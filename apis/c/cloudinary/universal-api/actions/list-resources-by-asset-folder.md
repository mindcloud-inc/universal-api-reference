# Cloudinary: List Resources by Asset Folder

Retrieves resources from a specific Cloudinary asset folder.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources-by-asset-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources-by-asset-folder?connectionId=$CONNECTION_ID&assetFolder=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetFolder": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources-by-asset-folder?${params}`, {
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
| `assetFolder` | string | yes | The asset folder to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_cursor": "string",
      "resources": [
        {}
      ],
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next_cursor` | string |  |
| `resources` | array<object> |  |
| `total_count` | number |  |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /resources/by_asset_folder` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources-by-asset-folder.md) for the provider-specific parameters and requirements.

