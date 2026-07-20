# Create Image Collection with Picnie

Creates an image collection in Picnie from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-image-collection`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Create Image Collection](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_group_id` | body | `number` | yes | Template group ID to use for collection generation. |
| `project_id` | body | `number` | yes | Project ID that will own the generated image collection. |
| `output_image_quality` | body | `string` | no | Optional image quality: Maximum, High, Medium, or Low. |
| `output_image_format` | body | `string` | no | Optional output format: jpg, png, gif, or webp. |
| `details` | body | `object<object>` | yes | Template field values to merge into every image in the collection. |
