# Assembly.com: List Tasks

Retrieves tasks from Assembly.com.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-tasks?${params}`, {
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
| `createdBy` | string | no | Filter tasks by the internal user that created the task. |
| `parentTaskId` | string | no | Filter tasks by parent task ID. |
| `status` | string | no | Filter tasks by status. One of todo, inProgress, completed. One of: `0`, `1`, `2`. |
| `clientId` | string | no | Filter tasks by assigned client user ID. |
| `internalUserId` | string | no | Filter tasks by assigned internal user ID. |
| `companyId` | string | no | Filter tasks by assigned company ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `GET /tasks` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

