# Set Baseline Image with Diffy

Sets a baseline image in Diffy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id/set-base-line-image/:screenshot_id`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Set Baseline Image](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakpoint` | body | `string` | no | Breakpoint for the baseline image. |
| `id` | path | `number` | yes | Project ID. |
| `screenshot_id` | path | `number` | yes | Screenshot ID. |
| `url` | body | `string` | no | Production page URL for the baseline image. |
