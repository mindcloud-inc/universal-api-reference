# List Tasks with GanttPRO

Retrieves tasks from a specific GanttPRO project.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [List Tasks](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `number` | yes | Required project identifier. GanttPRO accepts this as an array-style query parameter. Send multiple values as a array. |
