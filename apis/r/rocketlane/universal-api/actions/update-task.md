# Rocketlane: Update Task

Updates a task in Rocketlane.

```
PUT https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/update-task', {
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
| `includeFields` | list<string> | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `taskId` | number | no | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `taskName` | string | no | The **name** of the task. |
| `taskDescription` | string | no | The `description` of the task. The description body needs to be in **html** format to avoid any formatting issues in the application. |
| `taskPrivateNote` | string | no | The `privateNote` for the task is intended exclusively for team members. The note's content should be in `HTML` format to prevent any formatting issues in the application. |
| `startDate` | string | no | The date when a task starts its execution. It can be empty. The format for the start date is _YYYY-MM-DD_. |
| `dueDate` | string | no | The date when a task completes its execution. It can be empty. If both `startDate` and `dueDate` are specified for a given task, it is necessary that the latter should be on or after the given `startDate`. The format for the due date is _YYYY-MM-DD_. |
| `effortInMinutes` | number | no | The effort is the expected time required to complete the task. The value is determined in minutes. |
| `progress` | number | no | The task's progress, if indicated, will be available here and ranges in value from 0 to 100. The task's status can be used in place of this field, however progress can offer more precise data. |
| `atRisk` | boolean | no | Indicates whether the task has been marked as At Risk. This parameter is used to indicate that immediate action is necessary to unblock the task's execution. |
| `type` | string | no | The type of the task if specified will be available here. There are two options: `MILESTONE` or `TASK`. If a task is not explicitly marked as a milestone, it takes the default value as `TASK`. Milestones refer to critical tasks in the project that include an inbuilt CSAT capability that allows customers to offer CSAT evaluations depending on the task's execution. |
| `fields` | list<object> | no | The custom fields can be set during the task creation with the help of `fields`. The `fieldValue` can be either a string or a number or an array and it has to comply with the type of the field. Refer [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know how to assign `fieldValue` based on their `field_type`. |
| `status` | object | no | The value of the task status can be specified here and this is essential to keep track of it. |
| `externalReferenceId` | string | no | An externalReferenceId is a unique identifier that links entities or transactions between external systems and Rocketlane, ensuring accurate data correlation and consistency. |
| `private` | boolean | no | This depicts if the task is private or not. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assignees": {},
      "atRisk": true,
      "billable": true,
      "createdAt": 1,
      "createdBy": {},
      "csatEnabled": true,
      "dependencies": [
        {}
      ],
      "dueDate": "string",
      "dueDateActual": "string",
      "effortInMinutes": 1,
      "externalReferenceId": "string",
      "fields": [
        {}
      ],
      "financialsBudgets": [
        {}
      ],
      "followers": {},
      "parent": {},
      "phase": {},
      "priority": {},
      "private": true,
      "progress": 1,
      "project": {},
      "startDate": "string",
      "startDateActual": "string",
      "status": {},
      "taskDescription": "string",
      "taskId": 1,
      "taskName": "Ava Chen",
      "taskPrivateNote": "string",
      "timeEntryCategory": {},
      "type": "string",
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
| `billable` | boolean | Indicates whether the task is billable or non billable. |
| `createdAt` | number | The time when the task was created. The referenced time will be in epoch millis. |
| `createdBy` | object | The team member who updated the task. |
| `csatEnabled` | boolean | In case of milestone tasks, this field determines if a CSAT survey will be sent out on completion of the task |
| `dependencies` | array<object> | Task Dependencies allow you to define relationships between tasks that are dependent on each other. Note: Rocketlane allows you to have finish to start task dependencies. This means that dependent tasks are meant to start after the dependencies are marked as Complete. |
| `dueDate` | string | The date when a task completes its execution. It can be empty. If both `startDate` and `dueDate` are specified for a given task, it is necessary that the latter should be on or after the given `startDate`. The format for the due date is _YYYY-MM-DD_. |
| `dueDateActual` | string | The date on which the task status is changed to **Completed**. The status can be either the default status **Completed** or a custom status that is categorized as **Completed**. It will be null if the task is yet to be completed. The format for the actual due date is _YYYY-MM-DD_. |
| `effortInMinutes` | number | The effort is the expected time required to complete the task. The value is determined in minutes. |
| `externalReferenceId` | string | An externalReferenceId is a unique identifier that links entities or transactions between external systems and Rocketlane, ensuring accurate data correlation and consistency. |
| `fields` | array<object> | Fields lists the custom project fields whose values were provided during project creation or updated later. Refer these [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know more about different types of custom fields returned in response. |
| `financialsBudgets` | array<object> | The Financials budget in which the task's time entry is added. |
| `followers` | object | The task followers are the team members who keep track of the execution of the project. It can be either `members` (team members or customers) or `placeholders`. |
| `parent` | object | The parent task of the task. |
| `phase` | object | The `phase` associated with the task. |
| `priority` | object | Determines the level of priority of the task. |
| `private` | boolean | This depicts if the task is private or not. |
| `progress` | number | The task's progress, if indicated, will be available here and ranges in value from 0 to 100. The task's status can be used in place of this field, however progress can offer more precise data. |
| `project` | object | The `project` associated with task. |
| `startDate` | string | The date when a task starts its execution. It can be empty. The format for the start date is _YYYY-MM-DD_. |
| `startDateActual` | string | The date on which the task status is changed to **In Progress**. The status can be either the default (**In Progress**) status or a custom status that is categorized as **In Progress**. It can be null for tasks that have not yet begun. The format for the actual start date is _YYYY-MM-DD_. |
| `status` | object | The task status value and the label. v 10, l xyz. |
| `taskDescription` | string | The `description` of the task. The description body needs to be in **html** format to avoid any formatting issues in the application. |
| `taskId` | number | The task's unique, system-generated **identifier**, which can be used to identify the task globally. |
| `taskName` | string | The **name** of the task. |
| `taskPrivateNote` | string | The `privateNote` for the task is intended exclusively for team members. The note's content should be in `HTML` format to prevent any formatting issues in the application. |
| `timeEntryCategory` | object | The category in which the task's time entry is added. |
| `type` | string | The type of the task if specified will be available here. There are two options: `MILESTONE` or `TASK`. If a task is not explicitly marked as a milestone, it takes the default value as `TASK`. Milestones refer to critical tasks in the project that include an inbuilt CSAT capability that allows customers to offer CSAT evaluations depending on the task's execution. |
| `updatedAt` | number | The time when the task was last updated. Any changes that's related to the task are captured and specified here in epoch millis. |
| `updatedBy` | object | The team member who updated the task. |

## Native endpoint

Through the native Rocketlane API, this operation is `PUT /1.0/tasks/:taskId` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

