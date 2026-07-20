# Stack AI: Delete Folder



```
DELETE https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/delete-folder?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/delete-folder?${params}`, {
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
| `folderId` | string | yes | The folder identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": [
        "string"
      ],
      "group_id_access_list": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "personal_folder_owner_id": "string",
      "user_id_access_list": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | array<string> |  |
| `group_id_access_list` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `personal_folder_owner_id` | string |  |
| `user_id_access_list` | array<string> |  |

## Native endpoint

Through the native Stack AI API, this operation is `DELETE /folders/:folder_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

