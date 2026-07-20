# PixelBin.io: Update File

Updates an existing file in PixelBin.io.

```
PUT https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access` | string | no | Updated asset access level. |
| `fileId` | string | yes | Combined file path and file name for the file to update. |
| `isActive` | boolean | no | Whether the file remains active. |
| `metadata` | object | no | Updated metadata object for the file. |
| `name` | string | no | Updated file name. |
| `path` | string | no | Updated folder path. |
| `tags[]` | array<string> | no | Updated tags for the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "access": "string",
      "fileId": "string",
      "format": "string",
      "isActive": true,
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "thumbnail": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin file record ID. |
| `access` | string | Asset access level. |
| `fileId` | string | Combined PixelBin file path and name. |
| `format` | string | File format. |
| `isActive` | boolean | Whether the file is active. |
| `name` | string | File name. |
| `path` | string | Containing folder path. |
| `size` | number | File size in bytes. |
| `thumbnail` | string | Thumbnail URL when PixelBin provides one. |
| `url` | string | PixelBin CDN URL for the file. |

## Native endpoint

Through the native PixelBin.io API, this operation is `PATCH /service/platform/assets/v1.0/files/:fileId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file.md) for the provider-specific parameters and requirements.

