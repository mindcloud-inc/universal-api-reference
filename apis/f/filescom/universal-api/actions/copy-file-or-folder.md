# Files.com: Copy File or Folder

Copies a file or folder within Files.com.

```
POST https://connect.mindcloud.co/v1/universal/filescom/latest/actions/copy-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/copy-file-or-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filescom/latest/actions/copy-file-or-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "string",
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Existing file or folder path to copy, without leading or trailing slashes. |
| `destination` | string | yes | Destination path for the copied file or folder. |
| `overwrite` | boolean | no | Overwrite the destination if it already exists. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `copyBehaviors` | boolean | no | Copy permissions and related behaviors where supported. |
| `structure` | boolean | no | Preserve structure semantics during the copy when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_migration_id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_migration_id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `POST /file_actions/copy/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-file-or-folder.md) for the provider-specific parameters and requirements.

