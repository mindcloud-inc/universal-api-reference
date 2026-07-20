# HiDrive: Rename File

Renames a file in HiDrive.

```
PUT https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/rename-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/rename-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/rename-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | no | File path to rename. |
| `pid` | string | no | File public ID. |
| `name` | string | yes | New file name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ctime": 1,
      "id": "string",
      "image": {},
      "mime_type": "string",
      "mtime": 1,
      "name": "Ava Chen",
      "parent_id": "string",
      "path": "string",
      "readable": true,
      "size": 1,
      "type": "string",
      "writable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ctime` | number | Creation timestamp. |
| `id` | string | File object ID. |
| `image` | object | Image metadata when the file is an image. |
| `mime_type` | string | File MIME type. |
| `mtime` | number | Modified timestamp. |
| `name` | string | File name. |
| `parent_id` | string | Parent folder ID. |
| `path` | string | URL-encoded file path. |
| `readable` | boolean | Whether the file is readable. |
| `size` | number | File size in bytes. |
| `type` | string | Filesystem object type. |
| `writable` | boolean | Whether the file is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `POST /file/rename` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-file.md) for the provider-specific parameters and requirements.

