# Rocketlane: Remove Task Dependencies

Removes dependencies from a task in Rocketlane.

```
PUT https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-task-dependencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-task-dependencies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1,
  "dependencies": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-task-dependencies', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1,
    "dependencies": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `dependencies` | list<object> | yes | Task Dependencies allow you to define relationships between tasks that are dependent on each other. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "atRisk": true,
      "createdAt": 1,
      "createdBy": {},
      "dependencies": [
        {}
      ],
      "dueDate": "string",
      "effortInMinutes": 1,
      "fields": [
        {}
      ],
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
| `atRisk` | boolean | Indicates whether the task has been marked as At Risk. This parameter is used to indicate that immediate action is necessary to unblock the task's execution. |
| `createdAt` | number | The time when the task was created. The referenced time will be in epoch millis. |
| `createdBy` | object | The team member who updated the task. |
| `dependencies` | array<object> | Task Dependencies allow you to define relationships between tasks that are dependent on each other. Note: Rocketlane allows you to have finish to start task dependencies. This means that dependent tasks are meant to start after the dependencies are marked as Complete. |
| `dueDate` | string | The date when a task completes its execution. It can be empty. If both `startDate` and `dueDate` are specified for a given task, it is necessary that the latter should be on or after the given `startDate`. The format for the due date is _YYYY-MM-DD_. |
| `effortInMinutes` | number | The effort is the expected time required to complete the task. The value is determined in minutes. |
| `fields` | array<object> | Fields lists the custom project fields whose values were provided during project creation or updated later. Refer these [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know more about different types of custom fields returned in response. |
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

Through the native Rocketlane API, this operation is `POST /1.0/tasks/:taskId/remove-dependencies` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-task-dependencies.md) for the provider-specific parameters and requirements.

