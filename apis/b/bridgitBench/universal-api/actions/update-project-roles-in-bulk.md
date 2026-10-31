# Bridgit Bench: Update Project Roles in Bulk



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-roles-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-roles-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "payload[]": [
    {}
  ],
  "payload[].id": 1,
  "payload[].allocations[].startDate": "2026-05-07T12:00:00.000Z",
  "payload[].allocations[].endDate": "2026-05-07T12:00:00.000Z",
  "payload[].allocations[].allocatedPercent": 1,
  "payload[].removeSetup": true,
  "payload[].expandAllocations": true,
  "payload[].shiftDates": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-roles-in-bulk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "payload[]": [{}],
    "payload[].id": 1,
    "payload[].allocations[].startDate": "2026-05-07T12:00:00.000Z",
    "payload[].allocations[].endDate": "2026-05-07T12:00:00.000Z",
    "payload[].allocations[].allocatedPercent": 1,
    "payload[].removeSetup": true,
    "payload[].expandAllocations": true,
    "payload[].shiftDates": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes |  |
| `projectId` | number | yes |  |
| `payload[]` | array<object> | yes |  |
| `payload[].id` | number | yes |  |
| `payload[].taskId` | string | no | When taskId is included, the role is a task role. The taskId cannot be changed. |
| `payload[].name` | string | no |  |
| `payload[].startDate` | date | no |  |
| `payload[].endDate` | date | no |  |
| `payload[].skillSet[]` | array<number> | no |  |
| `payload[].note` | string | no |  |
| `payload[].categoryId` | number | no |  |
| `payload[].billable` | boolean | no |  |
| `payload[].allocations[]` | array<object> | no |  |
| `payload[].allocations[].startDate` | date | yes |  |
| `payload[].allocations[].endDate` | date | yes |  |
| `payload[].allocations[].allocatedPercent` | number | yes |  |
| `payload[].removeSetup` | boolean | yes |  |
| `payload[].expandAllocations` | boolean | yes |  |
| `payload[].shiftDates` | boolean | yes |  |
| `payload[].roleTagIds[]` | array<number> | no |  |
| `payload[].crewId` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PATCH /rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-roles-in-bulk.md) for the provider-specific parameters and requirements.

