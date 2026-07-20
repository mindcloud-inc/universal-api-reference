# Add Image Watermark with Picnie

Creates a watermarked image in Picnie using an image.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-watermark-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Add Image Watermark](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID that will own the watermarked image. |
| `background_image_url` | body | `string` | yes | Background image URL. |
| `front_image_url` | body | `string` | yes | Watermark image URL. |
| `position` | body | `string` | yes | Watermark position: tl, tc, tr, ml, mc, mr, bl, bc, or br. |
| `image_max_width` | body | `number` | yes | Maximum width of the watermark image. |
| `image_max_height` | body | `number` | yes | Maximum height of the watermark image. |
