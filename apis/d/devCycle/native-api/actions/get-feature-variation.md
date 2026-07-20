# Get Feature Variation with DevCycle

Retrieves a feature variation from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/variations/:key`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Feature Variation](https://docs.devcycle.com/management-api/#tag/Variations/operation/VariationsController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `key` | path | `string` | no | Variation key. |
| `project` | path | `string` | no | Project key. |
