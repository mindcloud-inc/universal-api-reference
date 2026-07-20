# Update Project Custom Day with GanttPRO

Updates a custom day in a GanttPRO project calendar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/customday/:customDayId`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Update Project Custom Day](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customDayId` | path | `number` | yes | GanttPRO custom day identifier. |
| `from` | body | `string` | no | Updated start date in YYYY-MM-DD format. |
| `to` | body | `string` | no | Updated end date in YYYY-MM-DD format. |
| `title` | body | `string` | no | Updated custom day title. |
