# HiDrive: Get Metadata

Retrieves file metadata from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-metadata?${params}`, {
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
| `fields` | string | no | Comma-separated metadata fields to include. |
| `path` | string | no | File or folder path. |
| `pid` | string | no | HiDrive public ID for the object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "ctime": 1,
      "id": "string",
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
| `category` | string | Object category. |
| `ctime` | number | Creation timestamp. |
| `id` | string | Filesystem object ID. |
| `mime_type` | string | MIME type for files. |
| `mtime` | number | Modified timestamp. |
| `name` | string | Object name when requested. |
| `parent_id` | string | Parent object ID. |
| `path` | string | URL-encoded object path. |
| `readable` | boolean | Whether the object is readable. |
| `size` | number | Object size in bytes where available. |
| `type` | string | Filesystem object type. |
| `writable` | boolean | Whether the object is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /meta` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metadata.md) for the provider-specific parameters and requirements.

