# Files.com: Move File or Folder

Moves a file or folder within Files.com.

```
PUT https://connect.mindcloud.co/v1/universal/filescom/latest/actions/move-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/move-file-or-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "sample.txt",
  "destination": "sample-moved.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filescom/latest/actions/move-file-or-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "sample.txt",
    "destination": "sample-moved.txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Existing file or folder path to move, without leading or trailing slashes. Default: `sample.txt`. |
| `destination` | string | yes | Destination path for the moved file or folder. Default: `sample-moved.txt`. |
| `overwrite` | boolean | no | Overwrite the destination if it already exists. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `POST /file_actions/move/:path` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-file-or-folder.md) for the provider-specific parameters and requirements.

