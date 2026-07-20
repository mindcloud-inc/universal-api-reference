# Stack AI: Get User Personal Folder



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-user-personal-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-user-personal-folder?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-user-personal-folder?${params}`, {
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
| `access` | array<string> | Accounts with access to the folder. |
| `group_id_access_list` | array<string> | Group IDs with folder access. |
| `id` | string | The folder identifier. |
| `name` | string | The folder name. |
| `personal_folder_owner_id` | string | The owner user identifier for the personal folder. |
| `user_id_access_list` | array<string> | User IDs with folder access. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /folders/me` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-personal-folder.md) for the provider-specific parameters and requirements.

