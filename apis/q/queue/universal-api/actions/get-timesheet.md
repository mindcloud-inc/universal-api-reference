# Queue: Get Timesheet

Retrieves a timesheet from Queue.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-timesheet?connectionId=$CONNECTION_ID&timesheetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timesheetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-timesheet?${params}`, {
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
| `timesheetId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billableRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "elapsedTime": 1,
      "endTime": "2026-05-07T12:00:00.000Z",
      "finished": true,
      "formattedDuration": "string",
      "hourlyRate": "https://example.com",
      "id": "string",
      "isActive": true,
      "notes": "string",
      "project": {},
      "shortFormattedDuration": {},
      "startTime": "2026-05-07T12:00:00.000Z",
      "task": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billableRate` | number |  |
| `createdAt` | date |  |
| `duration` | number |  |
| `elapsedTime` | number |  |
| `endTime` | date |  |
| `finished` | boolean |  |
| `formattedDuration` | string |  |
| `hourlyRate` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `notes` | string |  |
| `project` | object |  |
| `shortFormattedDuration` | object |  |
| `startTime` | date |  |
| `task` | object |  |
| `updatedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Queue API, this operation is `GET timesheets/:timesheet_id` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet.md) for the provider-specific parameters and requirements.

