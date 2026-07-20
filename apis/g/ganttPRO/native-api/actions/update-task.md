# Update Task with GanttPRO

Updates an existing task in GanttPRO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Update Task](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | GanttPRO task identifier. |
| `name` | body | `string` | no | Task name. |
| `description` | body | `string` | no | Task description. |
