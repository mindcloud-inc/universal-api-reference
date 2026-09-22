# Box: Get Folder



```
GET https://connect.mindcloud.co/v1/universal/box/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/box/latest/actions/get-folder?connectionId=$CONNECTION_ID&folderId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/box/latest/actions/get-folder?${params}`, {
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
| `folderId` | string | yes | The Box folder ID. Use `0` for the root folder. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional comma-separated list of folder fields to include in the response. Example: `id,type,name,parent,path_collection,size`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "item_status": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parent": {},
      "path_collection": {},
      "size": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the folder was created. |
| `description` | string | Optional folder description. |
| `id` | string | The folder ID. |
| `item_status` | string | The item status. |
| `modified_at` | date | When the folder was last modified. |
| `name` | string | The folder name. |
| `parent` | object | The parent folder. |
| `path_collection` | object | The folder path from the root. |
| `size` | number | The total size of the folder contents in bytes. |
| `type` | string | Always folder. |

## Native endpoint

Through the native Box API, this operation is `GET /folders/:folder_id` (base URL `https://api.box.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

