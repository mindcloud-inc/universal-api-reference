# Update Task with Avaza

Updates an existing task in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Task`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Task](https://api.avaza.com/#!/Task/Task_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TaskID` | body | `number` | yes | — |
| `FieldsToUpdate` | body | `list<string>` | yes | — |
| `SectionIDFK` | body | `number` | no | — |
| `Title` | body | `string` | no | — |
| `Description` | body | `string` | no | — |
| `AssignedToUserIDFK` | body | `list<number>` | yes | — |
| `DateStart` | body | `date` | no | — |
| `DateDue` | body | `date` | no | — |
| `TaskPriorityCode` | body | `string` | no | — |
| `EstimatedEffort` | body | `number` | no | Decimal hours |
| `TaskStatusCode` | body | `string` | no | — |
| `PercentComplete` | body | `number` | no | — |
| `Tags` | body | `list<object>` | yes | — |
| `Name` | body | `string` | no | — |
| `Color` | body | `string` | no | Hex color code in format #000000 |
