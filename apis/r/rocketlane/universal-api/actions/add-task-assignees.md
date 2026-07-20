# Rocketlane: Add Task Assignees

Adds assignees to a task in Rocketlane.

```
PUT https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/add-task-assignees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/add-task-assignees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/add-task-assignees', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `members` | list<object> | no | The list includes both `team members` and `customers` assigned to the task. |
| `placeholders` | list<object> | no | Rocketlane's placeholders are associated with roles. Based on the kind of roles and expertise that are needed to execute a task, placeholders can be added as assignees to templates as well as projects. Eventually, you can resolve placeholders by replacing them with team members according to their availability and role. Note: If the project is not built using sources, this value will be ignored but the mappings are retained and can be used in the future |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assignees": {},
      "atRisk": true,
      "createdAt": 1,
      "createdBy": {},
      "dueDate": "string",
      "effortInMinutes": 1,
      "fields": [
        {}
      ],
      "followers": {},
      "private": true,
      "progress": 1,
      "project": {},
      "startDate": "string",
      "status": {},
      "taskDescription": "string",
      "taskId": 1,
      "taskName": "Ava Chen",
      "updatedAt": 1,
      "updatedBy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | The field `archived` denotes whether the task is archived or not. The task if archived will not be available in all search requests. |
| `assignees` | object | The users who are assigned the responsibility to execute the task. The assignees can be either **members** (team members or customers) or **placeholders**. |
| `atRisk` | boolean | Indicates whether the task has been marked as At Risk. This parameter is used to indicate that immediate action is necessary to unblock the task's execution. |
| `createdAt` | number | The time when the task was created. The referenced time will be in epoch millis. |
| `createdBy` | object | The team member who updated the task. |
| `dueDate` | string | The date when a task completes its execution. It can be empty. If both `startDate` and `dueDate` are specified for a given task, it is necessary that the latter should be on or after the given `startDate`. The format for the due date is _YYYY-MM-DD_. |
| `effortInMinutes` | number | The effort is the expected time required to complete the task. The value is determined in minutes. |
| `fields` | array<object> | Fields lists the custom project fields whose values were provided during project creation or updated later. Refer these [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know more about different types of custom fields returned in response. |
| `followers` | object | The task followers are the team members who keep track of the execution of the project. It can be either `members` (team members or customers) or `placeholders`. |
| `private` | boolean | This depicts if the task is private or not. |
| `progress` | number | The task's progress, if indicated, will be available here and ranges in value from 0 to 100. The task's status can be used in place of this field, however progress can offer more precise data. |
| `project` | object | The `project` associated with task. |
| `startDate` | string | The date when a task starts its execution. It can be empty. The format for the start date is _YYYY-MM-DD_. |
| `status` | object | The task status value and the label. v 10, l xyz. |
| `taskDescription` | string | The `description` of the task. The description body needs to be in **html** format to avoid any formatting issues in the application. |
| `taskId` | number | The task's unique, system-generated **identifier**, which can be used to identify the task globally. |
| `taskName` | string | The **name** of the task. |
| `updatedAt` | number | The time when the task was last updated. Any changes that's related to the task are captured and specified here in epoch millis. |
| `updatedBy` | object | The team member who updated the task. |

## Native endpoint

Through the native Rocketlane API, this operation is `POST /1.0/tasks/:taskId/add-assignees` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-task-assignees.md) for the provider-specific parameters and requirements.

