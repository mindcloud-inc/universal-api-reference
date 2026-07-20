# List Allocations with Meisterplan

Retrieves a list of project allocations from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/allocations`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [List Allocations](https://api.us.meisterplan.com/docs/api.html#operation/GetAllAllocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
