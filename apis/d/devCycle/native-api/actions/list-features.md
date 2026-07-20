# List Features with DevCycle

Retrieves features from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project/features`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Features](https://docs.devcycle.com/management-api/#tag/Features-v2/operation/FeaturesController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | no | Project key. |
