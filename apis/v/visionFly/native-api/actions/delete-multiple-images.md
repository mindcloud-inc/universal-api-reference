# Delete Multiple Images with VisionFly

Deletes multiple images from the VisionFly CDN.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/cdn/images`
- **Base URL:** `https://api.visionfly.ai`
- **Official documentation:** [Delete Multiple Images](https://api.visionfly.ai/docs#/default/delete_images_cdn_images_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageIds[]` | body | `array<string>` | yes | Array of VisionFly image identifiers to delete. |
