# Update Project with Viqeo

Updates an existing project in Viqeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/media-platform/v1/project/:projectId`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Update Project](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `title` | body | `string` | no | Optional project name. |
