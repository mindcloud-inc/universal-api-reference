# Clockify: Add Manager Role to User

Adds the manager role to a user in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/add-manager-role-to-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/add-manager-role-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "entityId": "string",
  "role": "PROJECT_MANAGER"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/add-manager-role-to-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "entityId": "string",
    "role": "PROJECT_MANAGER"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "role": {
        "id": "string",
        "name": "Ava Chen",
        "source": {
          "id": "string",
          "type": "string"
        }
      },
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `role` | object |  |
| `role.id` | string |  |
| `role.name` | string |  |
| `role.source` | object |  |
| `role.source.id` | string |  |
| `role.source.type` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/users/:userId/roles` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-manager-role-to-user.md) for the provider-specific parameters and requirements.

