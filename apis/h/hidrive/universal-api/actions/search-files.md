# HiDrive: Search Files

Finds files in HiDrive by search query.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/search-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/search-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/search-files?${params}`, {
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
| `category` | string | no | Filter by file category, such as directory. |
| `fields` | string | no | Comma-separated metadata fields to include. |
| `mimeType` | string | no | Filter by MIME type, such as image/*. |
| `path` | string | no | Search root path. |
| `pid` | string | no | HiDrive public ID for the search root. |
| `pattern` | string<string> | no | Filename pattern to search for. Repeat this parameter only if the API caller needs multiple patterns. |
| `limit` | number | no | Maximum number of search results. |

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
      "path": "string",
      "result": [
        {}
      ],
      "size": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Result category. |
| `ctime` | number | Creation timestamp. |
| `id` | string | Result object ID. |
| `mime_type` | string | MIME type for file results. |
| `mtime` | number | Modified timestamp. |
| `path` | string | Result object path. |
| `result` | array<object> | Search result filesystem objects. |
| `size` | number | Result size in bytes. |
| `type` | string | Result filesystem object type. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /search` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-files.md) for the provider-specific parameters and requirements.

