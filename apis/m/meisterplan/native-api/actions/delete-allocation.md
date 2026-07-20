# Delete Allocation with Meisterplan

Deletes an existing project allocation from Meisterplan.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/allocations/:allocationId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Delete Allocation](https://api.us.meisterplan.com/docs/api.html#operation/DeleteAllocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `allocationId` | path | `string` | yes | Internal Meisterplan allocation identifier. |
