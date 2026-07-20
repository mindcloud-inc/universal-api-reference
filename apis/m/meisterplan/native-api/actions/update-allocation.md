# Update Allocation with Meisterplan

Updates an existing project allocation in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/allocations/:allocationId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Allocation](https://api.us.meisterplan.com/docs/api.html#operation/UpdateAllocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `allocationId` | path | `string` | yes | Internal Meisterplan allocation identifier. |
| `segments[]` | body | `array<object>` | yes | Updated array of allocation segments. |
