# PixelBin.io: Update Folder

Updates an existing folder in PixelBin.io.

```
PUT https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string",
  "isActive": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string",
    "isActive": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes |  |
| `isActive` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin folder identifier. |
| `isActive` | boolean | Whether the folder is active. |
| `name` | string | Folder name. |
| `path` | string | Parent folder path. |

## Native endpoint

Through the native PixelBin.io API, this operation is `PATCH /service/platform/assets/v1.0/folders/:folderId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

