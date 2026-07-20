# Get Feature Staleness with DevCycle

Retrieves staleness details for a feature from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project/features/:feature/staleness`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Feature Staleness](https://docs.devcycle.com/management-api/#tag/Features-v2/operation/FeaturesController_getStaleness)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
