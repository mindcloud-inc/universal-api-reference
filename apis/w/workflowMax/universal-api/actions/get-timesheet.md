# WorkflowMax: Get Timesheet



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-timesheet?connectionId=$CONNECTION_ID&timesheetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timesheetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-timesheet?${params}`, {
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
| `timesheetId` | string | yes | The WorkflowMax timesheet UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "createdAt": "string",
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
      "submittedAt": "string",
      "time": 1,
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean | Indicates if the timesheet entry is billable. |
| `createdAt` | string | The UTC date and time when the timesheet was created. |
| `customFields[].name` | string | The name for the timesheet entry's custom field. |
| `customFields[].uuid` | string | The unique identifier for the timesheet entry's custom field. |
| `customFields[].value` | string | The value for the timesheet entry's custom field. |
| `date` | string | The date of the timesheet entry. |
| `endTime` | string | The end time of the timesheet entry. Only populate when have value. |
| `job.jobNumber` | string | The job number of the job associated with the timesheet entry. |
| `job.name` | string | The job name of the job associated with the timesheet entry. |
| `job.uuid` | string | The unique identifier of the job associated with the timesheet entry. |
| `jobTask.label` | string | The label of the job task associated with the timesheet entry. |
| `jobTask.name` | string | The name of the job task associated with the timesheet entry. |
| `jobTask.uuid` | string | The unique identifier of the job task associated with the timesheet entry. |
| `note` | string | Additional notes or comments related to the timesheet entry. |
| `staff.firstName` | string | The first name of the staff associated with the timesheet entry. |
| `staff.lastName` | string | The last name of the staff associated with the timesheet entry. |
| `staff.uuid` | string | The unique identifier of the staff associated with the timesheet entry. |
| `startTime` | string | The start time of the timesheet entry. Only populate when have value. |
| `submittedAt` | string | The UTC date and time when the timesheet entry was submitted. |
| `time` | number | The time in minutes of the timesheet entry. |
| `updatedAt` | string | The UTC date and time when the timesheet was last updated. |
| `uuid` | string | The unique identifier of the timesheet entry. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/timesheets/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet.md) for the provider-specific parameters and requirements.

