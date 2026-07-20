# Add Task Dependencies with Rocketlane

Adds dependencies to a task in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/tasks/:taskId/add-dependencies`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Add Task Dependencies](https://developer.rocketlane.com/reference/add-dependencies-to-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `dependencies` | body | `list<object>` | yes | Task Dependencies allow you to define relationships between tasks that are dependent on each other. |
