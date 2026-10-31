# Bridgit Bench: Create Project Task Roles in Bulk



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-roles-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-roles-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "id": "string",
  "payload[]": [
    {}
  ],
  "payload[].name": "Ava Chen",
  "payload[].skillSet[]": [
    1
  ],
  "payload[].billable": true,
  "payload[].allocatedPercent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-roles-in-bulk', {
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
    "payload[]": [{}],
    "payload[].name": "Ava Chen",
    "payload[].skillSet[]": [1],
    "payload[].billable": true,
    "payload[].allocatedPercent": 1
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
| `payload[]` | array<object> | yes |  |
| `payload[].name` | string | yes |  |
| `payload[].skillSet[]` | array<number> | yes |  |
| `payload[].note` | string | no |  |
| `payload[].billable` | boolean | yes |  |
| `payload[].allocatedPercent` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id/roles/bulk` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-task-roles-in-bulk.md) for the provider-specific parameters and requirements.

