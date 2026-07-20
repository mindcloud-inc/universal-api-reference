# Feishu Drive: Create File Shortcut

Creates a file shortcut in Feishu Drive.

```
POST https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/create-file-shortcut
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/create-file-shortcut" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parentToken": "string",
  "referToken": "string",
  "referType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/create-file-shortcut', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parentToken": "string",
    "referToken": "string",
    "referType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentToken` | string | yes | Destination parent folder token for the shortcut. |
| `referToken` | string | yes | Source file token for the shortcut target. |
| `referType` | string | yes | Source file type for the shortcut target. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "succ_shortcut_node": {
          "name": "Ava Chen",
          "parent_token": "string",
          "shortcut_info": {
            "target_token": "string",
            "target_type": "string"
          },
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
| `data.succ_shortcut_node.name` | string |  |
| `data.succ_shortcut_node.parent_token` | string |  |
| `data.succ_shortcut_node.shortcut_info.target_token` | string |  |
| `data.succ_shortcut_node.shortcut_info.target_type` | string |  |
| `data.succ_shortcut_node.token` | string |  |
| `data.succ_shortcut_node.type` | string |  |
| `data.succ_shortcut_node.url` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Drive API, this operation is `POST /drive/v1/files/create_shortcut` (base URL `https://open.feishu.cn/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-shortcut.md) for the provider-specific parameters and requirements.

