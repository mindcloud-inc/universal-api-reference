# Update Task Comment with GanttPRO

Updates an existing task comment in GanttPRO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/:commentId`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Update Task Comment](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `number` | yes | GanttPRO comment identifier. |
| `content` | body | `string` | yes | Updated comment content. |
