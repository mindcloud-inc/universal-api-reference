# Get Story with Viqeo

Retrieves a story record from Viqeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/media-platform/v1/project/:projectId/story/:storyId`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Get Story](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `storyId` | path | `string` | yes | Story identifier from the path. |
