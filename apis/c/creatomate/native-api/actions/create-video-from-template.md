# Create Video From Template with Creatomate

Creates a video render from a template in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Create Video From Template](https://creatomate.com/docs/api/quick-start/create-a-video-by-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | The ID of the video template to render. |
| `modifications` | body | `object` | no | A key-value object of template modifications. |
