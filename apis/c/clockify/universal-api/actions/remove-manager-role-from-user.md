# Clockify: Remove Manager Role from User

Removes the manager role from a user in Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-manager-role-from-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-manager-role-from-user?connectionId=$CONNECTION_ID&workspaceId=string&userId=string&entityId=string&role=PROJECT_MANAGER" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "userId": "string",
  "entityId": "string",
  "role": "PROJECT_MANAGER"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-manager-role-from-user?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |
| `entityId` | string | yes |  |
| `role` | list<string> | yes | One of: `PROJECT_MANAGER`, `TEAM_MANAGER`, `WORKSPACE_ADMIN`. |
| `sourceType` | list<string> | no | One of: `USER_GROUP`. Example: `STANDARD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityId": "string",
      "role": "string",
      "sourceType": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityId` | string | The identifier of the related entity scope. |
| `role` | string | The role that was removed. |
| `sourceType` | string | The source type associated with the removed role. |
| `userId` | string | The identifier of the user whose manager role was removed. |

## Native endpoint

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/users/:userId/roles` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-manager-role-from-user.md) for the provider-specific parameters and requirements.

