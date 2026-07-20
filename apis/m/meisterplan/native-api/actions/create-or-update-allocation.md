# Create Or Update Allocation with Meisterplan

Creates or updates project allocations in Meisterplan.

## Endpoint

- **Method:** `POST`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/allocations`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Create Or Update Allocation](https://api.us.meisterplan.com/docs/api.html#operation/CreateOrUpdateAllocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `allocatedEntity` | body | `object` | yes | Allocated entity object with id, type, and optional projectRole. |
| `segments[]` | body | `array<object>` | no | Array of allocation segments. |
