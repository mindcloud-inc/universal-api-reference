# Remove Background with Picnie

Creates a background-removed image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/remove-background`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Remove Background](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID that will own the output image. |
| `image_url` | body | `string` | yes | Image URL to remove the background from. |
