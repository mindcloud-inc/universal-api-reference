# Add Task Assignees with Rocketlane

Adds assignees to a task in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/tasks/:taskId/add-assignees`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Add Task Assignees](https://developer.rocketlane.com/reference/add-assignee-to-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `members` | body | `list<object>` | no | The list includes both `team members` and `customers` assigned to the task. |
| `placeholders` | body | `list<object>` | no | Rocketlane's placeholders are associated with roles.  Based on the kind of roles and expertise that are needed to execute a task, placeholders can be added as assignees to templates as well as projects. Eventually, you can resolve placeholders by replacing them with team members according to their availability and role. Note: If the project is not built using sources, this value will be ignored but the mappings are retained and can be used in the future |
