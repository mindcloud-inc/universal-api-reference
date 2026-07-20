# List Project Stale Features with DevCycle

Retrieves stale features for a project from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:key/staleness`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [List Project Stale Features](https://docs.devcycle.com/management-api/#tag/Projects/operation/ProjectsController_getStaleness)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | no | Project key. |
