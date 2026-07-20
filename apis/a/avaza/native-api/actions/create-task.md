# Create Task with Avaza

Creates a new task in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Task`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Task](https://api.avaza.com/#!/Task/Task_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectIDFK` | body | `number` | yes | — |
| `SectionIDFK` | body | `number` | yes | — |
| `AccountTaskTypeIDFK` | body | `number` | no | — |
| `Title` | body | `string` | yes | — |
| `Description` | body | `string` | no | — |
| `AssignedToUserIDFKs` | body | `list<number>` | yes | — |
| `TaskPriorityCode` | body | `string` | no | — |
| `DateStart` | body | `date` | no | — |
| `DateDue` | body | `date` | no | — |
| `EstimatedEffort` | body | `number` | no | Decimal hours |
| `Tags` | body | `list<object>` | yes | Collection of tags specifying Name and Color (Hex) |
| `Name` | body | `string` | no | — |
| `Color` | body | `string` | no | Hex color code in format #000000 |
