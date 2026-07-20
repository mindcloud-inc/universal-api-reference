# List Custom Properties with DevCycle

Retrieves custom properties from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/customProperties`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Custom Properties](https://docs.devcycle.com/management-api/#tag/Custom-Properties/operation/CustomPropertiesController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | no | Project key. |
