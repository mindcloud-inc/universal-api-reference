# List Audiences with DevCycle

Retrieves audiences from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/audiences`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Audiences](https://docs.devcycle.com/management-api/#tag/Audiences/operation/AudiencesController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | no | Project key. |
