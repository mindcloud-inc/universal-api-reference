# Clockify: Search Workspace Users

Finds workspace users in Clockify by filters.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-workspace-users?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-workspace-users?${params}`, {
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
| `workspaceId` | list<string> | yes | Workspace identifier from Clockify. |
| `name` | string | no | Filter users by name. |
| `email` | string | no | Filter users by email. |
| `status` | list<string> | no | Filter by workspace membership statuses. One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `accountStatuses` | list<string> | no | Filter by account statuses. One of: `ACTIVE`, `DELETED`, `LIMITED`, `LIMITED_DELETED`, `NOT_REGISTERED`, `PENDING_EMAIL_VERIFICATION`. Accepts multiple values as an array. |
| `includeRoles` | boolean | no | Include role information in response. |
| `memberships` | list<string> | no | Filter by memberships. One of: `ALL`, `NONE`, `PROJECT`, `USERGROUP`, `WORKSPACE`. |
| `projectId` | string | no | Filter by project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeWorkspace": "string",
      "defaultWorkspace": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "profilePicture": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeWorkspace` | string |  |
| `defaultWorkspace` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `profilePicture` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/users/info` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workspace-users.md) for the provider-specific parameters and requirements.

