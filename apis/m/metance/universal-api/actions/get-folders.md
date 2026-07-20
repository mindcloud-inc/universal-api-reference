# Metance: Get Folders

Retrieves folders from the current Metance workspace.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-folders?${params}`, {
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
      "contentCount": 1,
      "folderLevel": 1,
      "folderName": "Ava Chen",
      "iconUrl": "https://example.com",
      "id": 1,
      "isGlobalShare": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentCount` | number | Content count |
| `folderLevel` | number | Folder level |
| `folderName` | string | Folder name |
| `iconUrl` | string | Folder icon URL |
| `id` | number | Folder ID |
| `isGlobalShare` | boolean | Whether the folder is globally shared |

## Native endpoint

Through the native Metance API, this operation is `GET /folders` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folders.md) for the provider-specific parameters and requirements.

