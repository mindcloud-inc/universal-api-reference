# List Feature Variations with DevCycle

Retrieves feature variations from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/variations`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Feature Variations](https://docs.devcycle.com/management-api/#tag/Variations/operation/VariationsController_findAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
