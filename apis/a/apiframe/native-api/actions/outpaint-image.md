# Outpaint Image with Apiframe

Creates an image outpainting task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/outpaint`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Outpaint Image](https://docs.apiframe.ai/api-endpoints/outpaint-zoom-out)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parent_task_id` | body | `string` | yes |
| `zoom_ratio` | body | `number` | yes |
