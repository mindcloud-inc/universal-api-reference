# Ringg AI: List Workspace Users

Retrieves workspace users from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/list-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/list-workspace-users?${params}`, {
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
      "workspaceUsers": [
        {
          "email": "ava@example.com",
          "id": "string",
          "inviteStatus": "string",
          "role": "string",
          "username": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workspaceUsers` | array<object> |  |
| `workspaceUsers[].email` | string |  |
| `workspaceUsers[].id` | string |  |
| `workspaceUsers[].inviteStatus` | string |  |
| `workspaceUsers[].role` | string |  |
| `workspaceUsers[].username` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /workspace/users` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-users.md) for the provider-specific parameters and requirements.

