# Get Feature Overrides with DevCycle

Retrieves overrides for a feature from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/overrides`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Feature Overrides](https://docs.devcycle.com/management-api/#tag/Overrides/operation/OverridesController_findOverridesForFeature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
