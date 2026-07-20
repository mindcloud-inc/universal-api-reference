# Feishu Drive: Copy File

Creates a file copy in Feishu Drive.

```
POST https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/copy-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/copy-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileToken": "string",
  "folderToken": "string",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/copy-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileToken": "string",
    "folderToken": "string",
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileToken` | string | yes | Source file token to copy. |
| `folderToken` | string | yes | Destination folder token for the copied file. |
| `name` | string | yes | Name for the copied file. |
| `type` | string | yes | Source file type, such as file or docx. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "file": {
          "name": "Ava Chen",
          "parent_token": "string",
          "token": "string",
          "type": "string",
          "url": "https://example.com"
        }
      },
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
| `data.file.name` | string |  |
| `data.file.parent_token` | string |  |
| `data.file.token` | string |  |
| `data.file.type` | string |  |
| `data.file.url` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Drive API, this operation is `POST /drive/v1/files/:file_token/copy` (base URL `https://open.feishu.cn/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-file.md) for the provider-specific parameters and requirements.

