# Get Custom Property with DevCycle

Retrieves a custom property from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/customProperties/:key`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Custom Property](https://docs.devcycle.com/management-api/#tag/Custom-Properties/operation/CustomPropertiesController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | no | Custom property key. |
| `project` | path | `string` | no | Project key. |
