# Lark Drive: Get Root Folder Meta



```
GET https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-root-folder-meta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-root-folder-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-root-folder-meta?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "id": "string",
        "token": "string",
        "user_id": "string"
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
| `data.id` | string |  |
| `data.token` | string |  |
| `data.user_id` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Lark Drive API, this operation is `GET /drive/explorer/v2/root_folder/meta` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-root-folder-meta.md) for the provider-specific parameters and requirements.

