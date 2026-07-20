# List Task Assignments with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/task/assignments`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Task Assignments](https://docs.checkflow.io/docs/api/tasks#get-task-assignments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigneeId` | query | `number` | yes | The assignee ID to list assignments for. |
| `assigneeType` | query | `number` | yes | The assignee type. Use 1 for member and 2 for group. |
| `includeTeamMemberGroups` | query | `boolean` | no | Whether to include tasks assigned via groups the member belongs to. |
| `includeCompletedTasks` | query | `boolean` | no | Whether to include completed tasks in the results. |
