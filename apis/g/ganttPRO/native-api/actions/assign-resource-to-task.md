# Assign Resource To Task with GanttPRO

Assigns resources to an existing GanttPRO task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/assignResource`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Assign Resource To Task](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | GanttPRO task identifier. |
| `resources[]` | body | `array<object>` | yes | Resource assignment objects, each with resourceId and resourceValue. |
