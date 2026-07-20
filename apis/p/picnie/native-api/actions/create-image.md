# Create Image with Picnie

Creates an image in Picnie from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Create Image](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID that will own the generated image. |
| `template_id` | body | `number` | yes | Template ID to use for image generation. |
| `template_name` | body | `string` | yes | Template name expected by Picnie. |
| `output_image_quality` | body | `string` | no | Optional image quality: Maximum, High, Medium, or Low. |
| `output_image_format` | body | `string` | no | Optional output format: jpg, png, gif, or webp. |
| `details` | body | `object<object>` | yes | Template field values to merge into the generated image. |
