# Delete Story with Viqeo

Deletes an existing story from Viqeo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/media-platform/v1/project/:projectId/story/:storyId`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Delete Story](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `storyId` | path | `string` | yes | Story identifier from the path. |
