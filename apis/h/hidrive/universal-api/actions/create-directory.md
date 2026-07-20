# HiDrive: Create Directory

Creates a new directory in HiDrive.

```
POST https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-directory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onExist` | string | no | Conflict behavior, such as autoname. |
| `path` | string | yes | Directory path to create. |
| `pid` | string | no | Optional parent directory public ID. |

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

Through the native HiDrive API, this operation is `POST /dir` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-directory.md) for the provider-specific parameters and requirements.

