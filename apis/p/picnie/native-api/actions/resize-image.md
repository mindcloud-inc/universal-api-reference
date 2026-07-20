# Resize Image with Picnie

Creates a resized image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/resize-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Resize Image](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID that will own the resized image. |
| `image_url` | body | `string` | yes | Image URL to resize. |
| `resize_type` | body | `string` | yes | 1 for height and width, 2 for percentage resize. |
| `height` | body | `number` | yes | Target height when resize type is 1. |
| `width` | body | `number` | yes | Target width when resize type is 1. |
| `resize_percentage` | body | `number` | no | Resize percentage when resize type is 2. |
| `no_enlarge_on_smaller` | body | `string` | no | Set to 1 to avoid enlarging smaller images. |
| `is_maintain_aspect_ratio` | body | `string` | no | Set to 1 to preserve aspect ratio. |
