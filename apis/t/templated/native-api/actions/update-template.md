# Update Template with Templated

Updates an existing template in Templated.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/template/:id`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Update Template](https://templated.io/docs/templates/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The template ID of the template you want to update. |
| `replaceLayers` | query | `boolean` | no | When true, layers not included in the request will be removed. |
| `name` | body | `string` | no | The name of the template. |
| `width` | body | `number` | no | The width of the template in pixels. |
| `height` | body | `number` | no | The height of the template in pixels. |
| `description` | body | `string` | no | A description of the template. |
| `layers[]` | body | `array<object>` | no | Layer updates for the template. |
| `pages[]` | body | `array<object>` | no | Page updates for a multi-page template. |
