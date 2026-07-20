# List My Projects with Taskade

Retrieves your personal projects from Taskade.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/projects`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List My Projects](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/me/projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Optional Taskade sort order (`viewed-asc` or `viewed-desc`). |
