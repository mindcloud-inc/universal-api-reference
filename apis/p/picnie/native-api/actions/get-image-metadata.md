# Get Image Metadata with Picnie

Retrieves JPEG image metadata from Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/get-image-metadata`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Get Image Metadata](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID for metadata lookup. |
| `image_url` | body | `string` | yes | JPEG image URL to inspect for metadata. |
