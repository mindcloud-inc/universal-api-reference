# Workday: Create Timesheet Entry

Create a worker time block in Workday Time Tracking for a specific worker using either quantity-based or clock-in and clock-out entry fields.

```
POST https://connect.mindcloud.co/v1/universal/workday/latest/actions/create-timesheet-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workday/latest/actions/create-timesheet-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workday/latest/actions/create-timesheet-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workerId` | string | yes | The Workday ID of the worker for whom the time block will be created. |
| `calendarDate` | date | no | Required for hourly entry together with Reported Quantity. |
| `reportedQuantity` | number | no | Required for hourly entry together with Calendar Date. |
| `inTime` | date | no | Required for in/out entry together with Out Time, In Time Zone ID, and Out Time Zone ID. |
| `outTime` | date | no | Required for in/out entry together with In Time, In Time Zone ID, and Out Time Zone ID. |
| `inTimeZone` | object | no | Reference object for the in time zone. |
| `inTimeZone.id` | string | no | The Workday ID for the selected in time zone reference. |
| `outTimeZone` | object | no | Reference object for the out time zone. |
| `outTimeZone.id` | string | no | The Workday ID for the selected out time zone reference. |
| `timeEntryCode` | object | no | Reference object for the selected time entry code. |
| `timeEntryCode.id` | string | no | The Workday ID for the selected time entry code reference. |
| `project` | object | no | Reference object for the selected project. |
| `project.id` | string | no | The Workday ID for the selected project reference. |
| `projectPlanTask` | object | no | Reference object for the selected project plan task. |
| `projectPlanTask.id` | string | no | The Workday ID for the selected project plan task reference. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Workday API returns.

## Native endpoint

Through the native Workday API, this operation is `POST workers/:ID/workerTimeBlock` (base URL `{{credentials.restAPIBaseURL}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-timesheet-entry.md) for the provider-specific parameters and requirements.

