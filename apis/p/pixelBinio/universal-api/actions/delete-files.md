# PixelBin.io: Delete Files

Deletes multiple files from PixelBin.io storage.

```
DELETE https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-files?connectionId=$CONNECTION_ID&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-files?${params}`, {
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
| `ids[]` | array<string> | yes | Array of file record IDs to delete. |

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
| `_id` | string | PixelBin file record ID for each deleted file. |
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

Through the native PixelBin.io API, this operation is `POST /service/platform/assets/v1.0/files/delete` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-files.md) for the provider-specific parameters and requirements.

