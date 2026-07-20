# HiDrive: Move File

Moves a file in HiDrive.

```
PUT https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/move-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/move-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dst": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/move-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dst": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dstId` | string | no | Destination parent public ID. |
| `src` | string | no | Source file path. |
| `srcId` | string | no | Source file public ID. |
| `dst` | string | yes | Destination file path. |

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

Through the native HiDrive API, this operation is `POST /file/move` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-file.md) for the provider-specific parameters and requirements.

