# Automate Team - Task Management: List Task Users



```
GET https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-task-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automate Team - Task Management `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-task-users?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceFilter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceFilter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-task-users?${params}`, {
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
| `workspaceFilter` | string | yes | PostgREST filter for the workspace id, for example eq.33371. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailFilter` | string | no | Optional PostgREST filter for email, for example ilike.*@example.com*. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Automate Team - Task Management API, this operation is `GET /rest/v1/user_profile` (base URL `https://api.automatebusiness.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-task-users.md) for the provider-specific parameters and requirements.

