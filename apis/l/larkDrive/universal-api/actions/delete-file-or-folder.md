# Lark Drive: Delete File or Folder



```
DELETE https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/delete-file-or-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/delete-file-or-folder?connectionId=$CONNECTION_ID&fileToken=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileToken": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/delete-file-or-folder?${params}`, {
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
| `fileToken` | string | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "task_id": "string"
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
| `data.task_id` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Lark Drive API, this operation is `DELETE /drive/v1/files/:file_token` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file-or-folder.md) for the provider-specific parameters and requirements.

