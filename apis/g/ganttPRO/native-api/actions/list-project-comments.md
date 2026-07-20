# List Project Comments with GanttPRO

Retrieves comments for a specific GanttPRO project.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/getByProjectId`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [List Project Comments](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `number` | yes | Project identifier used to list project comments. |
