# Create Project with Viqeo

Creates a new project in Viqeo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/media-platform/v1/project`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Create Project](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Unique project identifier, for example 1, 42, or coca_cola. |
| `title` | body | `string` | no | Optional project name. |
