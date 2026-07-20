# WorkflowMax: List Job Tasks



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-job-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-job-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-job-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
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
          "dueDate": "string",
          "estimatedMinutes": 1,
          "job": {
            "jobName": "Ava Chen",
            "jobNumber": "string",
            "uuid": "string"
          },
          "label": "string",
          "name": "Ava Chen",
          "notes": [
            {
              "comments": [
                {
                  "comment": "string",
                  "createdAt": "string",
                  "createdBy": {
                    "firstName": "Ava",
                    "lastName": "Chen",
                    "uuid": "string"
                  },
                  "updatedAt": "string"
                }
              ],
              "createdAt": "string",
              "createdBy": {
                "firstName": "Ava",
                "lastName": "Chen",
                "uuid": "string"
              },
              "date": "string",
              "description": "string",
              "title": "string",
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
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
          "timesheets": [
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
              "finishTime": "string",
              "minutes": 1,
              "note": "string",
              "staff": {
                "firstName": "Ava",
                "lastName": "Chen",
                "uuid": "string"
              },
              "startTime": "string",
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "to-dos": [
            {
              "completed": true,
              "completedBy": {
                "firstName": "Ava",
                "lastName": "Chen",
                "uuid": "string"
              },
              "completedDate": "string",
              "createdAt": "string",
              "name": "Ava Chen",
              "order": 1,
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].actualMinutes` | number | The actual time in minutes of the job task. |
| `data[].billable` | boolean | Indicate whether the job task is billable. |
| `data[].completedAt` | string | The date when the job task was completed. |
| `data[].createdAt` | string | The timestamp indicating when the job task was created. |
| `data[].customBillableRate` | number | The job custom rate of the job task when the task invoice rate is task billable rate. |
| `data[].customFields[].name` | string | The name of the custom field. |
| `data[].customFields[].uuid` | string | The unique identifier of the custom field. |
| `data[].customFields[].value` | string | The value of the custom field. |
| `data[].description` | string | The description of the job task. |
| `data[].dueDate` | string | The due date of the job task. |
| `data[].estimatedMinutes` | number | The estimated time in minutes of the job task. |
| `data[].job.jobName` | string | The name of the job which the job task belongs to. |
| `data[].job.jobNumber` | string | The number of the job which the job task belongs to. |
| `data[].job.uuid` | string | The unique identifier of the job which the job task belongs to. |
| `data[].label` | string | The label of the job task. |
| `data[].name` | string | The task name of the job task. |
| `data[].notes[].comments[].comment` | string | The detail of the comment. |
| `data[].notes[].comments[].createdAt` | string | The timestamp indicating when the comment was created. |
| `data[].notes[].comments[].createdBy.firstName` | string | The first name of the staff who added comment in the job task note. |
| `data[].notes[].comments[].createdBy.lastName` | string | The last name of the staff who added comment in the job task note. |
| `data[].notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who added comment in the job task note. |
| `data[].notes[].comments[].updatedAt` | string | The timestamp indicating when the comment was last updated. |
| `data[].notes[].createdAt` | string | The timestamp indicating when the job task note was created. |
| `data[].notes[].createdBy.firstName` | string | The first name of the staff who created the job task note. |
| `data[].notes[].createdBy.lastName` | string | The last name of the staff who created the job task note. |
| `data[].notes[].createdBy.uuid` | string | The unique identifier of the staff who created the job task note. |
| `data[].notes[].date` | string | The date of the job task note. |
| `data[].notes[].description` | string | The description of the job task note. |
| `data[].notes[].title` | string | The title of the job task note. |
| `data[].notes[].updatedAt` | string | The timestamp indicating when the job task note was last updated. |
| `data[].notes[].uuid` | string | The unique identifier of the job task note. |
| `data[].order` | number | The order of the job task. |
| `data[].phase.name` | string | The name of the phase of the job task. |
| `data[].phase.uuid` | string | The unique identifier of the phase of the job task. |
| `data[].staff[].allocatedTime` | number | The allocated time in minutes of the staff for the job task. |
| `data[].staff[].firstName` | string | The first name of the staff. |
| `data[].staff[].lastName` | string | The last name of the staff. |
| `data[].staff[].uuid` | string | The unique identifier of the staff. |
| `data[].startDate` | string | The start date of the job task. |
| `data[].taskUUID` | string | The unique identifier of the associated task of the job task. |
| `data[].timesheets[].billable` | boolean | Indicate whether the timesheet is billable. |
| `data[].timesheets[].createdAt` | string | The timestamp indicating when the timesheet was created. |
| `data[].timesheets[].customFields[].name` | string | The name of the timesheet custom field. |
| `data[].timesheets[].customFields[].uuid` | string | The unique identifier of the timesheet custom field. |
| `data[].timesheets[].customFields[].value` | string | The value of the timesheet custom field. |
| `data[].timesheets[].date` | string | The date of the timesheet. |
| `data[].timesheets[].finishTime` | string | The finish time of the timesheet. It only returns when it's available. |
| `data[].timesheets[].minutes` | number | The time in minutes of the timesheet. |
| `data[].timesheets[].note` | string | The note of the timesheet. |
| `data[].timesheets[].staff.firstName` | string | The first name of the staff for the timesheet. |
| `data[].timesheets[].staff.lastName` | string | The last name of the staff for the timesheet. |
| `data[].timesheets[].staff.uuid` | string | The unique identifier of the staff for the timesheet. |
| `data[].timesheets[].startTime` | string | The start time of the timesheet. It only returns when it's available. |
| `data[].timesheets[].updatedAt` | string | The timestamp indicating when the timesheet was last updated. |
| `data[].timesheets[].uuid` | string | The unique identifier of the timesheet. |
| `data[].to-dos[].completed` | boolean | Indicate whether the job task to-do item was completed. |
| `data[].to-dos[].completedBy.firstName` | string | The first name of the staff who completed the job task to-do item. |
| `data[].to-dos[].completedBy.lastName` | string | The last name of the staff who completed the job task to-do item. |
| `data[].to-dos[].completedBy.uuid` | string | The unique identifier of the staff who completed the job task to-do item. |
| `data[].to-dos[].completedDate` | string | The date when the job task to-do item was completed. |
| `data[].to-dos[].createdAt` | string | The timestamp indicating when the job task to-do item was created. |
| `data[].to-dos[].name` | string | The name of the job task to-do item. |
| `data[].to-dos[].order` | number | The order of the job task to-do item. |
| `data[].to-dos[].updatedAt` | string | The timestamp indicating when the job task to-do item was last updated. |
| `data[].to-dos[].uuid` | string | The unique identifier of the job task to-do item. |
| `data[].updatedAt` | string | The timestamp indicating when the job task was updated. |
| `data[].uuid` | string | The unique identifier of the job task. |
| `total` | number | The total number of job tasks returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/jobs/tasks` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-job-tasks.md) for the provider-specific parameters and requirements.

