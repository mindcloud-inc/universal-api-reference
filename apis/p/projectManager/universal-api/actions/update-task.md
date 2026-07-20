# ProjectManager: Update Task

Updates an existing task in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "22222222-2222-2222-2222-222222222222"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "22222222-2222-2222-2222-222222222222"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The unique identifier of the Task to update Example: `22222222-2222-2222-2222-222222222222`. |
| `name` | string | no | The common name of this Task. Example: `MindCloud Sample`. |
| `description` | string | no | A description of the work to be performed in this Task. Example: `MindCloud sample description.`. |
| `percentComplete` | number | no | The numerical percentage, from 0-100, representing the percentage completion for this Task. Any numbers below zero or above 100 will be clamped to the minimum or maximum value. This value can be edited manually in the Gantt chart view of the application, or can be selected on the Task Detail page within the Kanban board. Example: `1`. |
| `statusId` | string | no | The TaskStatus assigned to this Task. Example: `88888888-8888-8888-8888-888888888888`. |
| `priorityId` | number | no | The unique identifier of the TaskPriority Example: `88888888-8888-8888-8888-888888888888`. |
| `plannedStartDate` | string | no | The date when work on this Task is planned to begin. This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace. For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time). This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. Example: `2026-04-10`. |
| `plannedFinishDate` | string | no | The date when work on this Task is expected to complete. This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace. For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time). This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. Example: `2026-04-10`. |
| `plannedDuration` | number | no | The planned duration (in minutes) for this Task. Cannot be negative. Example: `1`. |
| `plannedEffort` | number | no | The planned effort (in minutes) for this Task. Cannot be negative. Example: `1`. |
| `plannedCost` | number | no | The planned cost for this Task. Cannot be negative. Example: `1`. |
| `actualStartDate` | string | no | If set, this is the actual date when work began on the Task. This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace. For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time). This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. Example: `2026-04-10`. |
| `actualFinishDate` | string | no | If set, this is the actual date when work was completed on the Task. This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace. For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time). This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. Example: `2026-04-10`. |
| `actualDuration` | number | no | The actual duration (in minutes) for this Task. Cannot be negative. Example: `1`. |
| `actualCost` | number | no | If set, this represents the actual tracked cost for this Task. Example: `1`. |
| `theme` | string | no | Color theme definition for this task. eg. Blue, Brown, DarkBlue, DarkGrey, Gold, Green, Grey, LightBrown, LightGreen, LightGrey, LightPurple, LightYellow, Magenta, Mauve, Navy, Orange, Purple, Red. Example: `sample-theme`. |
| `isLocked` | boolean | no | Unlocked tasks can be adjusted by changes to their dependencies, resource leveling, or other factors. All tasks are unlocked by default. If a task is set to `IsLocked` = `true`, the dates and assigned resources are locked for this task and will not be automatically changed by any process. Example: `true`. |
| `isMilestone` | boolean | no | True if this task is a milestone. Milestones represent a specific point in time for the project. When a milestone is locked, it represents a fixed time within the project that can be used to relate to other tasks. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changeSetId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeSetId` | string |  |
| `id` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `PUT /api/data/tasks/:taskId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

