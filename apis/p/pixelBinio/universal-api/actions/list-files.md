# PixelBin.io: List Files

Retrieves files and folders from PixelBin.io storage.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-files?${params}`, {
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
| `format` | string | no | Find items with a matching format. |
| `name` | string | no | Find items with a matching name. |
| `onlyFiles` | boolean | no | If true, fetch only files. Default: `false`. |
| `path` | string | no | Find items with a matching path. |
| `onlyFolders` | boolean | no | If true, fetch only folders. Default: `false`. |
| `pageNo` | number | no | Page number. Default: `1`. |
| `pageSize` | number | no | Page size. Default: `10`. |
| `sort` | string | no | Key to sort results by. Use -suffix for descending order. Default: `name`. |

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
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin asset or folder identifier. |
| `access` | string | Asset access level when the row is a file. |
| `fileId` | string | Combined asset path and filename when the row is a file. |
| `format` | string | File format when the row is a file. |
| `name` | string | Asset or folder name. |
| `path` | string | Containing folder path. |
| `size` | number | File size in bytes when the row is a file. |
| `type` | string | Resource type returned by PixelBin. |
| `url` | string | CDN URL when the row is a file. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/assets/v1.0/listFiles` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

