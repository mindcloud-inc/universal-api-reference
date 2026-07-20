# Files.com: List Folder Contents

Retrieves folder contents by path from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-folder-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-folder-contents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-folder-contents?${params}`, {
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
| `modifiedAtDatetime` | date | no | Return only items modified after this timestamp. Use only together with Type. |
| `path` | string | no | Folder path without leading or trailing slashes. Leave blank to list the Files.com site root. |
| `searchCustomMetadataKey` | string | no | When Search is set, restrict the search to a specific custom metadata key, or use `*` to match any key. |
| `search` | string | no | Search for items by name within the selected folder. |
| `searchAll` | boolean | no | Search the entire Files.com site when true. Do not send Path at the same time. |
| `type` | string | no | Limit results to `file` or `folder` items. |
| `perPage` | number | no | Maximum number of entries to return in one page. |
| `cursor` | string | no | Cursor token returned by a previous folder-list response page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_metadata": {},
      "display_name": "Ava Chen",
      "is_locked": true,
      "mtime": "2026-05-07T12:00:00.000Z",
      "path": "string",
      "permissions": "string",
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
| `created_at` | date |  |
| `custom_metadata` | object |  |
| `display_name` | string |  |
| `is_locked` | boolean |  |
| `mtime` | date |  |
| `path` | string |  |
| `permissions` | string |  |
| `size` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /folders/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-folder-contents.md) for the provider-specific parameters and requirements.

