# Remove Resource From Task with GanttPRO

Removes resources from an existing GanttPRO task.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/assignResource`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Remove Resource From Task](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | GanttPRO task identifier. |
| `resourceId` | query | `number` | yes | Resource identifier or identifiers to remove from the task. Send multiple values as a array. |
