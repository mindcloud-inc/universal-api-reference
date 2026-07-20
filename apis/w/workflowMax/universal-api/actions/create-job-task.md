# WorkflowMax: Create Job Task



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobIdentifier` | string | yes | The WorkflowMax job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualMinutes": 1,
      "billable": true,
      "completedAt": "string",
      "createdAt": "string",
      "customBillableRate": 1,
      "customFields": [
        {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      ],
      "description": "string",
      "endDate": "string",
      "estimatedMinutes": 1,
      "job": {
        "jobName": "Ava Chen",
        "jobNumber": "string",
        "uuid": "string"
      },
      "label": "string",
      "name": "Ava Chen",
      "order": 1,
      "phase": {
        "name": "Ava Chen",
        "uuid": "string"
      },
      "staff": [
        {
          "allocatedTime": 1,
          "firstName": "Ava",
          "lastName": "Chen",
          "uuid": "string"
        }
      ],
      "startDate": "string",
      "taskUUID": "string",
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
| `actualMinutes` | number | The actual minutes of the job task. |
| `billable` | boolean | Indicate whether the job task is billable or not. |
| `completedAt` | string | The date in local time when the job task is completed. |
| `createdAt` | string | The UTC timestamp indicating when the job task was created. |
| `customBillableRate` | number | The custom billable rate of the job task. |
| `customFields[].name` | string | The name of the custom field. |
| `customFields[].uuid` | string | The unique identifier of the custom field. |
| `customFields[].value` | string | The value of the custom field. |
| `description` | string | The description of the job task. |
| `endDate` | string | The date in local time when the job task is ended. |
| `estimatedMinutes` | number | The estimated minutes of the job task. |
| `job.jobName` | string | The name of the job associated with the job task. |
| `job.jobNumber` | string | The number of the job associated with the job task. |
| `job.uuid` | string | The unique identifier of the job associated with the job task. |
| `label` | string | The label of the job task. |
| `name` | string | The name of the job task. |
| `order` | number | The order of the job task. |
| `phase.name` | string | The name of the phase which the job task belongs to. |
| `phase.uuid` | string | The unique identifier of the phase which the job task belongs to. |
| `staff[].allocatedTime` | number | The allocated time allocated to the staff for the job task. |
| `staff[].firstName` | string | The first name of the staff who is allocated to the job task. |
| `staff[].lastName` | string | The last name of the staff who is allocated to the job task. |
| `staff[].uuid` | string | The unique identifier of the staff who is allocated to the job task. |
| `startDate` | string | The date in local time when the job task is started. |
| `taskUUID` | string | The unique identifer of the task as managed in the task admin. |
| `updatedAt` | string | The UTC timestamp indicating when the job task was last updated. |
| `uuid` | string | The unique identifer of the job task. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/jobs/{identifier}/tasks` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-task.md) for the provider-specific parameters and requirements.

