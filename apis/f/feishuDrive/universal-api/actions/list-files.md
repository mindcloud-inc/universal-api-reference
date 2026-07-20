# Feishu Drive: List Files

Retrieves files from Feishu Drive.

```
GET https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/list-files?${params}`, {
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
| `folderToken` | string | no | Optional folder token. Leave empty to list the root Drive folder. |
| `pageSize` | number | no | Optional page size for paginated folder listings. |
| `pageToken` | string | no | Optional page token returned by a previous list call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "files": [
          {
            "created_time": "string",
            "modified_time": "string",
            "name": "Ava Chen",
            "owner_id": "string",
            "parent_token": "string",
            "token": "string",
            "type": "string",
            "url": "https://example.com"
          }
        ],
        "has_more": true
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
| `data.files[].created_time` | string |  |
| `data.files[].modified_time` | string |  |
| `data.files[].name` | string |  |
| `data.files[].owner_id` | string |  |
| `data.files[].parent_token` | string |  |
| `data.files[].token` | string |  |
| `data.files[].type` | string |  |
| `data.files[].url` | string |  |
| `data.has_more` | boolean |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Drive API, this operation is `GET /drive/v1/files` (base URL `https://open.feishu.cn/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

