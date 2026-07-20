# Databricks: Delete Workspace Assignment

Deletes a workspace assignment from Databricks.

```
DELETE https://connect.mindcloud.co/v1/universal/databricks/latest/actions/delete-workspace-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/delete-workspace-assignment?connectionId=$CONNECTION_ID&workspaceId=1&principalId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "principalId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/delete-workspace-assignment?${params}`, {
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
| `principalId` | number | yes | The ID of the user, service principal, or group. |

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

Through the native Databricks API, this operation is `DELETE /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId/permissionassignments/principals/:principalId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workspace-assignment.md) for the provider-specific parameters and requirements.

