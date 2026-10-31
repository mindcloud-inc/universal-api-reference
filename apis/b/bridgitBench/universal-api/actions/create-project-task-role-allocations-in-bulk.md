# Bridgit Bench: Create Project Task Role Allocations in Bulk



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-role-allocations-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-role-allocations-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "taskId": "string",
  "payload[]": [
    {}
  ],
  "payload[].roleId": 1,
  "payload[].personId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-task-role-allocations-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "taskId": "string",
    "payload[]": [{}],
    "payload[].roleId": 1,
    "payload[].personId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `projectId` | number | yes | The project ID |
| `taskId` | string | yes | The task ID |
| `payload[]` | array<object> | yes |  |
| `payload[].roleId` | number | yes |  |
| `payload[].personId` | number | yes |  |
| `payload[].startDate` | date | no |  |
| `payload[].endDate` | date | no |  |
| `payload[].roleStartDate` | date | no | Optional. When provided, updates the unfilled role's start date before creating the allocation. Must be set together with ResourcePlanning.Contracts.ProjectAllocationRequest.RoleEndDate — supplying only one will fail validation. |
| `payload[].roleEndDate` | date | no | Optional. When provided, updates the unfilled role's end date before creating the allocation. Must be set together with ResourcePlanning.Contracts.ProjectAllocationRequest.RoleStartDate — supplying only one will fail validation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/allocations/bulk` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-task-role-allocations-in-bulk.md) for the provider-specific parameters and requirements.

