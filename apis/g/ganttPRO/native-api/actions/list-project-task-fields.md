# List Project Task Fields with GanttPRO

Retrieves task fields for a specific GanttPRO project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/taskFields`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [List Project Task Fields](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `number` | yes | Project identifier used to return task field definitions for one project. |
