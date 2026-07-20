# Get Environment with DevCycle

Retrieves an environment from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/environments/:key`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Environment](https://docs.devcycle.com/management-api/#tag/Environments/operation/EnvironmentsController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | no | Environment key. |
| `project` | path | `string` | no | Project key. |
