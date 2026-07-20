# File.io: List Files

Retrieves files from File.io.

```
GET https://connect.mindcloud.co/v1/universal/fileio/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileio/latest/actions/list-files?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "size": 1
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
| `name` | string | File name. |
| `size` | number | File size in bytes. |

## Native endpoint

Through the native File.io API, this operation is `GET /` (base URL `https://file.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

