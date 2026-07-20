# Feishu Drive: Create Folder

Creates a new folder in Feishu Drive.

```
POST https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderToken": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderToken": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderToken` | string | yes | Parent folder token. Use an empty string for the root folder. |
| `name` | string | yes | Folder name to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "token": "string",
        "url": "https://example.com"
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
| `data.token` | string |  |
| `data.url` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Drive API, this operation is `POST /drive/v1/files/create_folder` (base URL `https://open.feishu.cn/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

