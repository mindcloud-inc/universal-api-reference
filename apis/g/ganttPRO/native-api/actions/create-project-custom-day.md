# Create Project Custom Day with GanttPRO

Creates a custom day in a GanttPRO project calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/customday`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Create Project Custom Day](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `number` | yes | Project identifier for the custom day. |
| `from` | body | `string` | yes | Start date in YYYY-MM-DD format. |
| `to` | body | `string` | no | End date in YYYY-MM-DD format. |
| `title` | body | `string` | no | Custom day title. |
