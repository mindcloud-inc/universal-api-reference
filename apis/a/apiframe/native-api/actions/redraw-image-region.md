# Redraw Image Region with Apiframe

Creates an image region redraw task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/inpaint`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Redraw Image Region](https://docs.apiframe.ai/api-endpoints/inpaint-vary-region)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parent_task_id` | body | `string` | yes |
| `mask` | body | `string` | yes |
