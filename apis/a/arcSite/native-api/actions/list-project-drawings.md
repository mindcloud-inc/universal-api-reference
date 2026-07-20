# List Project Drawings with ArcSite

Retrieves drawings for a specific ArcSite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/drawings`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [List Project Drawings](https://dev.arcsite.com/#get-project-drawings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project. |
