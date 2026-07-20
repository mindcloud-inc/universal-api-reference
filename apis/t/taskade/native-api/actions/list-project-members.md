# List Project Members with Taskade

Retrieves members from a Taskade project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/members`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List Project Members](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/get-project-members)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
