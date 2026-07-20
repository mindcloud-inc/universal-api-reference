# Files.com: Create Folder

Creates a new folder in Files.com.

```
POST https://connect.mindcloud.co/v1/universal/filescom/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filescom/latest/actions/create-folder', {
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
| `path` | string | yes | Folder path to create, without leading or trailing slashes. |
| `mkdirParents` | boolean | no | Create missing parent folders automatically when true. |

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

Through the native Files.com API, this operation is `POST /folders/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

