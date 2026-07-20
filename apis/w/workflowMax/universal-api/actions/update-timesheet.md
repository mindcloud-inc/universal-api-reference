# WorkflowMax: Update Timesheet



```
PUT https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/update-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/update-timesheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timesheetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/update-timesheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timesheetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timesheetId` | string | yes | The WorkflowMax timesheet UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "customFields": [
        {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      ],
      "date": "string",
      "endTime": "string",
      "job": {
        "jobNumber": "string",
        "name": "Ava Chen",
        "uuid": "string"
      },
      "jobTask": {
        "label": "string",
        "name": "Ava Chen",
        "uuid": "string"
      },
      "note": "string",
      "staff": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "startTime": "string",
      "time": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean | Indicates whether the timesheet is billable or not. |
| `customFields[].name` | string | The name of the timesheet custom field. |
| `customFields[].uuid` | string | The unique identifier of the timesheet custom field. |
| `customFields[].value` | string | The value of the timesheet custom field. |
| `date` | string | The date of the timesheet. |
| `endTime` | string | The end time of the timesheet. It only returns when the Entry Mode is Start/Finish in the organization settings. |
| `job.jobNumber` | string | The job number of the job associated with the timesheet. |
| `job.name` | string | The name of the job associated with the timesheet. |
| `job.uuid` | string | The unique identifier of the job associated with the timesheet. |
| `jobTask.label` | string | The label of the job task associated with the timesheet. |
| `jobTask.name` | string | The name of the job task associated with the timesheet. |
| `jobTask.uuid` | string | The unique identifier of the job task associated with the timesheet. |
| `note` | string | Additional remarks or comments or the timesheet. |
| `staff.firstName` | string | The first name of the staff for the timesheet. |
| `staff.lastName` | string | The last name of the staff for the timesheet. |
| `staff.uuid` | string | The unique identifier of the staff for the timesheet. |
| `startTime` | string | The start time of the timesheet. It only returns when the Entry Mode is Start/Finish in the organization settings. |
| `time` | number | The time duration of the timesheet. |
| `uuid` | string | The unique identifier of the timesheet. |

## Native endpoint

Through the native WorkflowMax API, this operation is `PUT v2/timesheets/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timesheet.md) for the provider-specific parameters and requirements.

