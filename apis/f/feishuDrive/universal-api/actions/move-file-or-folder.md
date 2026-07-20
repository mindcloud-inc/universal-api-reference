# Feishu Drive: Move File or Folder

Moves a file or folder in Feishu Drive.

```
PUT https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/move-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/move-file-or-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileToken": "string",
  "folderToken": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/move-file-or-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileToken": "string",
    "folderToken": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileToken` | string | yes | File or folder token to move. |
| `folderToken` | string | yes | Destination folder token. |
| `type` | string | yes | File or folder type to move. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Drive API, this operation is `POST /drive/v1/files/:file_token/move` (base URL `https://open.feishu.cn/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-file-or-folder.md) for the provider-specific parameters and requirements.

