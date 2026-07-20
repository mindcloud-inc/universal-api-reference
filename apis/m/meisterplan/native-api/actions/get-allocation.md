# Get Allocation with Meisterplan

Retrieves a project allocation from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/projects/:projectId/allocations/:allocationId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Get Allocation](https://api.us.meisterplan.com/docs/api.html#operation/GetAllocationId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `allocationId` | path | `string` | yes | Internal Meisterplan allocation identifier. |
