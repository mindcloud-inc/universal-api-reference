# ProjectManager: Create Task

Creates a new task in ProjectManager.

```
POST https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11111111-1111-1111-1111-111111111111",
  "name": "MindCloud Sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11111111-1111-1111-1111-111111111111",
    "name": "MindCloud Sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The unique identifier of the Project that will contain this Task Example: `11111111-1111-1111-1111-111111111111`. |
| `name` | string | yes | The common name of this Task. Example: `MindCloud Sample`. |
| `description` | string | no | A description of the work to be performed in this Task. Example: `MindCloud sample description.`. |
| `percentComplete` | number | no | The numerical percentage, from 0-100, representing the percentage completion for this Task. Any numbers below zero or above 100 will be clamped to the minimum or maximum value. This value can be edited manually in the Gantt chart view of the application, or can be selected on the Task Detail page within the Kanban board. Example: `1`. |
| `statusId` | string | no | The unique identifier of the TaskStatus for this Task Example: `88888888-8888-8888-8888-888888888888`. |
| `priorityId` | number | no | A numerical value representing the Priority of this Task Example: `88888888-8888-8888-8888-888888888888`. |
| `assignees[]` | array<string> | no | A list of unique identifiers of TaskAssignees to be assigned to this Task Example: `sample`. |
| `assignees[]` | array<string> | no | A list of unique identifiers of TaskAssignees to be assigned to this Task Example: `sample`. |
| `assignees[]` | array<string> | no | A list of unique identifiers of TaskAssignees to be assigned to this Task Example: `sample`. |
| `plannedStartDate` | string | no | The date when work on this Task is planned to begin. Example: `2026-04-10`. |
| `plannedFinishDate` | string | no | The date when work on this Task is expected to complete. Example: `2026-04-10`. |
| `plannedDuration` | number | no | The planned duration (in minutes) for this Task. Cannot be negative. Example: `1`. |
| `plannedEffort` | number | no | The planned effort (in minutes) for this Task. Cannot be negative. Example: `1`. |
| `plannedCost` | number | no | The planned cost for this Task. Cannot be negative. Example: `1`. |
| `actualStartDate` | string | no | The date when work on this Task actually started, if known. Example: `2026-04-10`. |
| `actualCost` | number | no | The actual cost of this Task to date, if known. Example: `1`. |
| `theme` | string | no | Color theme definition for this task. eg. Blue, Brown, DarkBlue, DarkGrey, Gold, Green, Grey, LightBrown, LightGreen, LightGrey, LightPurple, LightYellow, Magenta, Mauve, Navy, Orange, Purple, Red. Example: `sample-theme`. |
| `isLocked` | boolean | no | Unlocked tasks can be adjusted by changes to their dependencies, resource leveling, or other factors. All tasks are unlocked by default. If a task is set to `IsLocked` = `true`, the dates and assigned resources are locked for this task and will not be automatically changed by any process. Example: `true`. |
| `isMilestone` | boolean | no | True if this task is a milestone. Milestones represent a specific point in time for the project. When a milestone is locked, it represents a fixed time within the project that can be used to relate to other tasks. Example: `true`. |
| `parentId` | string | no | Gets or sets the unique identifier of the parent task. If set, this task will be a child of the specified parent task, supporting task hierarchies and sub-tasks. Example: `88888888-8888-8888-8888-888888888888`. |
| `index` | number | no | Gets or sets the position of the task within the list of project tasks. Used to determine the order of tasks in the project with the first task being 1. Example: `1`. |

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

Through the native ProjectManager API, this operation is `POST /api/data/projects/:projectId/tasks` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

