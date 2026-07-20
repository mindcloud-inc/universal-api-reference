# Update Story with Viqeo

Updates an existing story in Viqeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/media-platform/v1/project/:projectId/story/:storyId`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Update Story](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `storyId` | path | `string` | yes | Story identifier from the path. |
| `title` | body | `string` | no | Optional story title. |
