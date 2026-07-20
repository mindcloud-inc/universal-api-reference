# File.io: Upload File

Uploads a file to File.io.

```
POST https://connect.mindcloud.co/v1/universal/fileio/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fileio/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File to upload as multipart/form-data. Required by File.io for file upload. |
| `expires` | string | no | Optional expiration duration such as 1d, 1w, 1M, or 1y. Example: `1d`. |
| `maxDownloads` | number | no | Optional maximum number of downloads before the file expires. Example: `1`. |
| `autoDelete` | boolean | no | Whether File.io should automatically delete the file after download or expiration. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoDelete": true,
      "created": "2026-05-07T12:00:00.000Z",
      "downloads": 1,
      "expires": "2026-05-07T12:00:00.000Z",
      "expiry": "string",
      "id": "string",
      "key": "string",
      "link": "https://example.com",
      "maxDownloads": 1,
      "mimeType": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "size": 1,
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoDelete` | boolean | Whether File.io auto-deletes the file. |
| `created` | date | Creation timestamp. |
| `downloads` | number | Number of downloads. |
| `expires` | date | Expiration timestamp. |
| `expiry` | string | Human-readable expiration window. |
| `id` | string | File identifier. |
| `key` | string | File.io download key. |
| `link` | string | Shareable File.io link. |
| `maxDownloads` | number | Maximum downloads before expiration. |
| `mimeType` | string | File MIME type. |
| `modified` | date | Last modification timestamp. |
| `name` | string | Uploaded file name. |
| `size` | number | File size in bytes. |
| `status` | number | Provider status code from File.io. |
| `success` | boolean | Whether File.io accepted the operation. |

## Native endpoint

Through the native File.io API, this operation is `POST /` (base URL `https://file.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

