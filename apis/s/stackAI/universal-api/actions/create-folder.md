# Stack AI: Create Folder



```
POST https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The folder name. |

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

Through the native Stack AI API, this operation is `PUT /folders` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

