# Get Feature with DevCycle

Retrieves a feature from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project/features/:feature`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Feature](https://docs.devcycle.com/management-api/#tag/Features-v2/operation/FeaturesController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feature` | path | `string` | no | Feature key. |
| `project` | path | `string` | no | Project key. |
