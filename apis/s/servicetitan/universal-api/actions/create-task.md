# ServiceTitan: Create Task



```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "reportedById": 1,
  "assignedToId": 1,
  "isClosed": true,
  "businessUnitId": 1,
  "employeeTaskTypeId": "string",
  "employeeTaskSourceId": "string",
  "reportedDate": "2026-05-07T12:00:00.000Z",
  "priority": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "reportedById": 1,
    "assignedToId": 1,
    "isClosed": true,
    "businessUnitId": 1,
    "employeeTaskTypeId": "string",
    "employeeTaskSourceId": "string",
    "reportedDate": "2026-05-07T12:00:00.000Z",
    "priority": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `projectId` | number | no |  |
| `jobId` | number | no |  |
| `customerId` | number | no |  |
| `description` | string | no |  |
| `reportedById` | number | yes |  |
| `assignedToId` | number | yes |  |
| `isClosed` | boolean | yes |  |
| `businessUnitId` | number | yes |  |
| `employeeTaskTypeId` | string | yes |  |
| `employeeTaskSourceId` | string | yes |  |
| `reportedDate` | date | yes |  |
| `priority` | string | yes |  |
| `employeeTaskResolutionId` | number | no |  |
| `completeBy` | date | no |  |
| `startedOn` | date | no |  |
| `involvedEmployeeIdList[]` | array | no |  |
| `status` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST taskmanagement/v2/tenant/{{credentials.tenant}}/tasks` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

