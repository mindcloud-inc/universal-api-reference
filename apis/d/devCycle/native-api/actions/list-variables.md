# List Variables with DevCycle

Retrieves variables from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/variables`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Variables](https://docs.devcycle.com/management-api/#tag/Variables/operation/VariablesController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | no | Project key. |
