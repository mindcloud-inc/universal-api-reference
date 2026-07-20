# Databricks: Update Workspace Assignment

Updates a workspace assignment in Databricks.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-workspace-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-workspace-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "principalId": 1,
  "permissions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-workspace-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "principalId": 1,
    "permissions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | The workspace ID. |
| `principalId` | number | yes | The ID of the user, service principal, or group. |
| `permissions` | list<string> | yes | Array of permissions assignments to update on the workspace. Valid values are "USER" and "ADMIN" (case-sensitive). If both "USER" and "ADMIN" are provided, "ADMIN" takes precedence. Other values will be ignored. Note that excluding this field, or providing unsupported values, will have the same effect as providing an empty list, which will result in the deletion of all permissions for the principal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "permissions": [
        "string"
      ],
      "principal": {
        "display_name": "Ava Chen",
        "principal_id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Assignment error, if any. |
| `permissions` | array<string> | Permissions granted to the principal. |
| `principal.display_name` | string | Display name for the principal. |
| `principal.principal_id` | number | Principal ID for the workspace assignment. |

## Native endpoint

Through the native Databricks API, this operation is `PUT /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId/permissionassignments/principals/:principalId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-assignment.md) for the provider-specific parameters and requirements.

