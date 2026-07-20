# List Allocated Tasks For Sprint with ITM Platform

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Projects/{ProjectId}/AllocatedTasks/{SprintId}`
- **Base URL:** `https://api.itmplatform.com/{company}`
- **Official documentation:** [List Allocated Tasks For Sprint](https://developers.itmplatform.com/documentation/#/operations/getAllocatedTasksForSprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectId` | path | `string` | yes | The ITM Platform project ID. |
| `SprintId` | path | `string` | yes | The ITM Platform sprint ID. |
