# Apply Image Filter with Picnie

Creates a filtered image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/filter-on-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Apply Image Filter](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Image URL to filter. |
| `filter` | body | `string` | yes | Filter constant such as IMG_FILTER_GRAYSCALE. |
| `project_id` | body | `number` | yes | Project ID that will own the filtered image. |
