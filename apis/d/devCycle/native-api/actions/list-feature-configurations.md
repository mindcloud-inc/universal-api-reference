# List Feature Configurations with DevCycle

Retrieves configurations for a feature from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/features/:feature/configurations`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Feature Configurations](https://docs.devcycle.com/management-api/#tag/Feature-Configurations/operation/FeatureConfigsController_findAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
