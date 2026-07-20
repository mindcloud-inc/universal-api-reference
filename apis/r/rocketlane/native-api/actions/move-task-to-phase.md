# Move Task To Phase with Rocketlane

Moves a task to a phase in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/tasks/:taskId/move-phase`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Move Task To Phase](https://developer.rocketlane.com/reference/move-task-to-given-phase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | The task's unique, system-generated **identifier**, which can be used to identify the task globally |
| `phase` | body | `object` | yes | The phase to which the task will be moved, associating the task with this phase. |
