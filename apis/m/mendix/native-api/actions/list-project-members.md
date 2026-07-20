# List Project Members with Mendix

Retrieves project team members from Mendix.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/members`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [List Project Members](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project-id` | path | `string` | yes | The unique identifier of a project. |
