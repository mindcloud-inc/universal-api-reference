# HiDrive: List Directory

Retrieves a directory from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-directory?${params}`, {
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
| `fields` | string | no | Comma-separated directory fields to include. |
| `members` | string | no | Directory member types to include, such as all. |
| `path` | string | no | Path to the directory. |
| `pid` | string | no | HiDrive public ID for the directory. |
| `sort` | string | no | Sort by name, category, mtime, type, or size. Prefix with - for descending. |
| `limit` | number | no | Maximum number of directory entries to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ctime": 1,
      "id": "string",
      "members": [
        {}
      ],
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
| `id` | string | Directory path-independent object ID. |
| `members` | array<object> | Directory members returned for the requested fields. |
| `mtime` | number | Modified timestamp. |
| `name` | string | Directory name. |
| `parent_id` | string | Parent directory object ID. |
| `path` | string | URL-encoded directory path. |
| `readable` | boolean | Whether the directory is readable. |
| `type` | string | Filesystem object type. |
| `writable` | boolean | Whether the directory is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /dir` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-directory.md) for the provider-specific parameters and requirements.

