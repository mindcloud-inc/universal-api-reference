# Bridgit Bench: Create Project Task Role



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "id": "string",
  "name": "Ava Chen",
  "skillSet[]": [
    1
  ],
  "billable": true,
  "allocatedPercent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "id": "string",
    "name": "Ava Chen",
    "skillSet[]": [1],
    "billable": true,
    "allocatedPercent": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `projectId` | number | yes | The project ID the task belongs to |
| `id` | string | yes | The task ID the task belongs to |
| `name` | string | yes |  |
| `skillSet[]` | array<number> | yes |  |
| `note` | string | no |  |
| `billable` | boolean | yes |  |
| `allocatedPercent` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id/roles` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-task-role.md) for the provider-specific parameters and requirements.

