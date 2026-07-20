# Files.com: Update File or Folder Metadata

Updates file or folder metadata in Files.com.

```
PUT https://connect.mindcloud.co/v1/universal/filescom/latest/actions/update-file-or-folder-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/update-file-or-folder-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filescom/latest/actions/update-file-or-folder-metadata', {
  method: 'PUT',
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
| `path` | string | yes | Existing file or folder path to update, without leading or trailing slashes. |
| `customMetadata` | object | no | JSON object of custom metadata fields to store on the file or folder. |
| `priorityColor` | string | no | Priority color label to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_metadata": {},
      "display_name": "Ava Chen",
      "is_locked": true,
      "mtime": "2026-05-07T12:00:00.000Z",
      "path": "string",
      "permissions": "string",
      "priority_color": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_metadata` | object |  |
| `display_name` | string |  |
| `is_locked` | boolean |  |
| `mtime` | date |  |
| `path` | string |  |
| `permissions` | string |  |
| `priority_color` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `PATCH /files/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file-or-folder-metadata.md) for the provider-specific parameters and requirements.

