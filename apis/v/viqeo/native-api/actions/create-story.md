# Create Story with Viqeo

Creates a new story in Viqeo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/media-platform/v1/project/:projectId/story`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Create Story](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `id` | body | `string` | yes | Unique story identifier, for example 42 or campaign_17. |
| `title` | body | `string` | no | Optional story title. |
