# Get Variable with DevCycle

Retrieves a variable from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/variables/:key`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Variable](https://docs.devcycle.com/management-api/#tag/Variables/operation/VariablesController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | no | Variable key. |
| `project` | path | `string` | no | Project key. |
