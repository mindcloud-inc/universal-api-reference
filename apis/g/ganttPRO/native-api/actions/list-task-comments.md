# List Task Comments with GanttPRO

Retrieves comments for a specific GanttPRO task.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [List Task Comments](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `number` | yes | Required task identifier. GanttPRO accepts this as an array-style query parameter. Send multiple values as a array. |
