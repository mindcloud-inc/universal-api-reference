# Move Task To List with KiteSuite

Moves a task to another list in KiteSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/list/task/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Move Task To List](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID. |
| `newListID` | body | `string` | yes | Destination list ID. |
| `position` | body | `string` | yes | Target position in the destination list. |
