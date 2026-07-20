# HiDrive: Move Directory

Moves a directory in HiDrive.

```
PUT https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/move-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/move-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dst": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/move-directory', {
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
| `src` | string | no | Source directory path. |
| `srcId` | string | no | Source directory public ID. |
| `dst` | string | yes | Destination directory path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ctime": 1,
      "id": "string",
      "mtime": 1,
      "name": "Ava Chen",
      "parent_id": "string",
      "path": "string",
      "readable": true,
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
| `id` | string | Directory object ID. |
| `mtime` | number | Modified timestamp. |
| `name` | string | Directory name. |
| `parent_id` | string | Parent directory object ID. |
| `path` | string | URL-encoded directory path. |
| `readable` | boolean | Whether the directory is readable. |
| `type` | string | Filesystem object type. |
| `writable` | boolean | Whether the directory is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `POST /dir/move` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-directory.md) for the provider-specific parameters and requirements.

