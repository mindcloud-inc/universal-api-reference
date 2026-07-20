# Compress Image with Picnie

Creates a compressed image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/compress-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Compress Image](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID that will own the compressed image. |
| `image_url` | body | `string` | yes | Image URL to compress. |
| `image_quality` | body | `number` | yes | Compression quality between 55 and 70. |
| `image_output_format` | body | `string` | yes | Output format. Use original, jpg, png, or webp. |
