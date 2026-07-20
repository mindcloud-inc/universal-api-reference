# SeaTable: List Files from Folder

Lists files from a SeaTable custom folder.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/list-files-from-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/list-files-from-folder?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/list-files-from-folder?${params}`, {
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
      "dir": [
        {}
      ],
      "file": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dir` | array<object> |  |
| `file` | array<object> |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api/v2.1/dtable/custom/app-asset-dir/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files-from-folder.md) for the provider-specific parameters and requirements.

