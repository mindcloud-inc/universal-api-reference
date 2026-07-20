# Extend Video with Apiframe

Creates a video extension task in Apiframe.

## Endpoint

- **Method:** `POST`
- **Path:** `/imagine-video-extend`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Extend Video](https://docs.apiframe.ai/api-endpoints/extend-video)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parent_task_id` | body | `string` | yes |
| `index` | body | `string` | yes |
| `prompt` | body | `string` | yes |
