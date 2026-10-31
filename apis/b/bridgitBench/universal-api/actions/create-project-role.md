# Bridgit Bench: Create Project Role



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "name": "Ava Chen",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "skillSet[]": [
    1
  ],
  "billable": true,
  "allocations[].startDate": "2026-05-07T12:00:00.000Z",
  "allocations[].endDate": "2026-05-07T12:00:00.000Z",
  "allocations[].allocatedPercent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "name": "Ava Chen",
    "startDate": "2026-05-07T12:00:00.000Z",
    "endDate": "2026-05-07T12:00:00.000Z",
    "skillSet[]": [1],
    "billable": true,
    "allocations[].startDate": "2026-05-07T12:00:00.000Z",
    "allocations[].endDate": "2026-05-07T12:00:00.000Z",
    "allocations[].allocatedPercent": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `projectId` | number | yes | The project ID the role belongs to |
| `name` | string | yes |  |
| `taskId` | string | no |  |
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |
| `skillSet[]` | array<number> | yes |  |
| `note` | string | no |  |
| `categoryId` | number | no |  |
| `billable` | boolean | yes |  |
| `allocations[]` | array<object> | no |  |
| `allocations[].startDate` | date | yes |  |
| `allocations[].endDate` | date | yes |  |
| `allocations[].allocatedPercent` | number | yes |  |
| `roleTagIds[]` | array<number> | no |  |
| `assignmentBreakdownBy` | list<string> | no | One of: `Custom`, `Monthly`, `Phases`, `Weekly`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/projects/:projectId/roles` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-role.md) for the provider-specific parameters and requirements.

