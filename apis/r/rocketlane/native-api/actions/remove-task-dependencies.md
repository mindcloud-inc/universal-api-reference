# Remove Task Dependencies with Rocketlane

Removes dependencies from a task in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/tasks/:taskId/remove-dependencies`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Remove Task Dependencies](https://developer.rocketlane.com/reference/remove-dependencies-from-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `dependencies` | body | `list<object>` | yes | Task Dependencies allow you to define relationships between tasks that are dependent on each other. |
