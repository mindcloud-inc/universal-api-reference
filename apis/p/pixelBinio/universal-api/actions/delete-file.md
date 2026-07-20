# PixelBin.io: Delete File

Deletes an existing file from PixelBin.io.

```
DELETE https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | Combined file path and file name for the file to delete. |

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
| `isActive` | boolean | Whether the file was active at delete time. |
| `name` | string | File name. |
| `path` | string | Containing folder path. |
| `size` | number | File size in bytes. |
| `thumbnail` | string | Thumbnail URL when PixelBin provides one. |
| `url` | string | PixelBin CDN URL for the file. |

## Native endpoint

Through the native PixelBin.io API, this operation is `DELETE /service/platform/assets/v1.0/files/:fileId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

