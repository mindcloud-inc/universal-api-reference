# Bridgit Bench: Update Project Tasks



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "payload[]": [
    {}
  ],
  "payload[].id": "string",
  "payload[].shiftDates": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-project-tasks', {
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
    "payload[].id": "string",
    "payload[].shiftDates": true
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
| `payload[]` | array<object> | yes |  |
| `payload[].id` | string | yes |  |
| `payload[].name` | string | no |  |
| `payload[].startDate` | date | no |  |
| `payload[].endDate` | date | no |  |
| `payload[].shiftDates` | boolean | yes | If this property is true and you specify a changed task start or end date in this request, then the task's start and end dates, and the start and end dates for all task roles will be adjusted by the same amount. If this property is set to true, then you must only send EITHER startDate OR endDate - behavior when setting both is to shift with the task start date |
| `payload[].shiftSubsequentTasks` | boolean | no | Used to shift subsequent tasks when the END DATE of this task is changed. If true, subsequent tasks will be shifted by the same number of days as this task |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/tasks` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-tasks.md) for the provider-specific parameters and requirements.

