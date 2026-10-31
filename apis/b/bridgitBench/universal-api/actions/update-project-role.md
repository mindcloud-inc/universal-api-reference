# Bridgit Bench: Update Project Role



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "id": 1,
  "payload": {},
  "payload.id": 1,
  "payload.removeSetup": true,
  "payload.expandAllocations": true,
  "payload.shiftDates": true,
  "payload.name": "Ava Chen",
  "payload.startDate": "2026-05-07T12:00:00.000Z",
  "payload.endDate": "2026-05-07T12:00:00.000Z",
  "payload.skillSet[]": [
    1
  ],
  "payload.billable": true,
  "payload.allocations[].startDate": "2026-05-07T12:00:00.000Z",
  "payload.allocations[].endDate": "2026-05-07T12:00:00.000Z",
  "payload.allocations[].allocatedPercent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "id": 1,
    "payload": {},
    "payload.id": 1,
    "payload.removeSetup": true,
    "payload.expandAllocations": true,
    "payload.shiftDates": true,
    "payload.name": "Ava Chen",
    "payload.startDate": "2026-05-07T12:00:00.000Z",
    "payload.endDate": "2026-05-07T12:00:00.000Z",
    "payload.skillSet[]": [1],
    "payload.billable": true,
    "payload.allocations[].startDate": "2026-05-07T12:00:00.000Z",
    "payload.allocations[].endDate": "2026-05-07T12:00:00.000Z",
    "payload.allocations[].allocatedPercent": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `projectId` | number | yes | The project ID that the role belongs to |
| `id` | number | yes | The role ID |
| `payload` | object | yes |  |
| `payload.id` | number | yes |  |
| `payload.removeSetup` | boolean | yes |  |
| `payload.expandAllocations` | boolean | yes |  |
| `payload.shiftDates` | boolean | yes |  |
| `payload.crewId` | number | no |  |
| `payload.startTime` | string | no |  |
| `payload.endTime` | string | no |  |
| `payload.workDays` | list<number> | no | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Accepts multiple values as an array. |
| `payload.name` | string | yes |  |
| `payload.taskId` | string | no |  |
| `payload.startDate` | date | yes |  |
| `payload.endDate` | date | yes |  |
| `payload.skillSet[]` | array<number> | yes |  |
| `payload.note` | string | no |  |
| `payload.categoryId` | number | no |  |
| `payload.billable` | boolean | yes |  |
| `payload.allocations[]` | array<object> | no |  |
| `payload.allocations[].startDate` | date | yes |  |
| `payload.allocations[].endDate` | date | yes |  |
| `payload.allocations[].allocatedPercent` | number | yes |  |
| `payload.roleTagIds[]` | array<number> | no |  |
| `payload.assignmentBreakdownBy` | list<string> | no | One of: `Custom`, `Monthly`, `Phases`, `Weekly`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-role.md) for the provider-specific parameters and requirements.

