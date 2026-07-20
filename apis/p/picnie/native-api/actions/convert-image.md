# Convert Image with Picnie

Creates a converted image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Convert Image](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Image URL to convert. |
| `output_format` | body | `string` | yes | Target output format such as webp. |
| `project_id` | body | `number` | yes | Project ID that will own the converted image. |
