# List Projects with Zeplin

Retrieves a list of projects from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Projects](https://docs.zeplin.dev/reference/getprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | query | `string` | no | Workspace of the project, it can be `personal` or the id of organization |
| `status` | query | `string` | no | Filter by status |
