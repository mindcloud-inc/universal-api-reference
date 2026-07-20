# Clockify: Remove User from Group

Removes a user from a group in Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-user-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-user-from-group?connectionId=$CONNECTION_ID&userGroupId=string&userId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userGroupId": "string",
  "userId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-user-from-group?${params}`, {
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
| `userGroupId` | string | yes |  |
| `userId` | string | yes |  |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "teamManagers": [
        [
          {}
        ]
      ],
      "userIds": [
        [
          "string"
        ]
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `teamManagers[]` | array<object> |  |
| `teamManagers[].id` | string |  |
| `teamManagers[].name` | string |  |
| `userIds[]` | array<string> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/user-groups/:userGroupId/users/:userId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-group.md) for the provider-specific parameters and requirements.

