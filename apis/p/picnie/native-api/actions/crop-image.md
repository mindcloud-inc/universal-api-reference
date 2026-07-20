# Crop Image with Picnie

Creates a cropped image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/crop-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Crop Image](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Image URL to crop. |
| `height` | body | `number` | yes | Target crop height. |
| `width` | body | `number` | yes | Target crop width. |
| `project_id` | body | `number` | yes | Project ID that will own the cropped image. |
| `vertical_crop_from` | body | `string` | yes | Vertical crop anchor: top, bottom, or center. |
| `horizontal_crop_from` | body | `string` | yes | Horizontal crop anchor: left, right, or center. |
