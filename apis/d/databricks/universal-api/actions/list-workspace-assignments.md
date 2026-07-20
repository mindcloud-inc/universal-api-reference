# Databricks: List Workspace Assignments

Retrieves workspace assignments from Databricks for a workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspace-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspace-assignments?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspace-assignments?${params}`, {
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
| `workspaceId` | number | yes | The workspace ID for the account. |

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
        "group_name": "Ava Chen",
        "principal_id": 1,
        "service_principal_name": "Ava Chen",
        "user_name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error response associated with a workspace permission assignment, if any. |
| `permissions` | array<string> | The permissions level of the principal. |
| `principal` | object | Information about the principal assigned to the workspace. |
| `principal.display_name` | string | The display name of the principal. |
| `principal.group_name` | string | The group name of the group. Present only if the principal is a group. |
| `principal.principal_id` | number | The unique, opaque id of the principal. |
| `principal.service_principal_name` | string | The name of the service principal. Present only if the principal is a service principal. |
| `principal.user_name` | string | The username of the user. Present only if the principal is a user. |

## Native endpoint

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId/permissionassignments` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-assignments.md) for the provider-specific parameters and requirements.

