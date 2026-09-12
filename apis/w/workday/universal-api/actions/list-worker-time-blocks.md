# Workday: List Worker Time Blocks

List worker time blocks from Workday Time Tracking so you can review timesheet-style entries by worker, date range, status, project, or task.

```
GET https://connect.mindcloud.co/v1/universal/workday/latest/actions/list-worker-time-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/list-worker-time-blocks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workday/latest/actions/list-worker-time-blocks?${params}`, {
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
| `worker` | string<string> | no | The Workday ID of the worker for the time block filter. |
| `fromDate` | date | no | Start date of the time block date range filter. |
| `toDate` | date | no | End date of the time block date range filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string<string> | no | The Workday ID of the approval status for the time block filter. |
| `phase` | string<string> | no | The Workday ID of the project plan phase filter. |
| `project` | string<string> | no | The Workday ID of the project filter. |
| `projectPlanTask` | string<string> | no | The Workday ID of the project plan task filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarDate": "2026-05-07T12:00:00.000Z",
      "comment": "string",
      "descriptor": "string",
      "id": "string",
      "inTime": "2026-05-07T12:00:00.000Z",
      "inTimeZone": {},
      "outTime": "2026-05-07T12:00:00.000Z",
      "outTimeZone": {},
      "project": {},
      "projectPlanTask": {},
      "reportedQuantity": 1,
      "status": {},
      "timeEntryCode": {},
      "worker": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarDate` | date | The calendar date for the time block. |
| `comment` | string | Comment on the time block when present. |
| `descriptor` | string | The display name of the worker time block. |
| `id` | string | The ID for the worker time block. |
| `inTime` | date | Clock-in time for in/out time blocks. |
| `inTimeZone` | object | Time zone information for the in time. |
| `outTime` | date | Clock-out time for in/out time blocks. |
| `outTimeZone` | object | Time zone information for the out time. |
| `project` | object | Project details when the time block is project-based. |
| `projectPlanTask` | object | Project plan task details when applicable. |
| `reportedQuantity` | number | Reported quantity for quantity-based time blocks. |
| `status` | object | Approval status details for the time block. |
| `timeEntryCode` | object | Time entry code details when applicable. |
| `worker` | object | Worker details for the time block. |

## Native endpoint

Through the native Workday API, this operation is `GET /workerTimeBlocks` (base URL `{{credentials.restAPIBaseURL}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-worker-time-blocks.md) for the provider-specific parameters and requirements.

