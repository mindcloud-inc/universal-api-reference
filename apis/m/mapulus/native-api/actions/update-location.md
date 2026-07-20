# Update Location with Mapulus

Updates an existing location in Mapulus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/locations/:id`
- **Base URL:** `https://api.mapulus.com`
- **Official documentation:** [Update Location](https://developer.mapulus.com/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location ID. |
| `layer_id` | body | `string` | yes | The layer that will contain the location. |
| `lat` | body | `number` | no | Latitude in decimal degrees. |
| `lon` | body | `number` | no | Longitude in decimal degrees. |
| `label` | body | `string` | no | Short label for the location. |
| `title` | body | `string` | no | Display title for the location. |
| `address` | body | `string` | no | Address for the location. |
| `external_id` | body | `string` | no | External identifier for the location. |
| `travel_contour` | body | `boolean` | no | Whether to generate a travel contour. |
| `contour_mode` | body | `string` | no | Routing mode for contour generation. |
| `contour_metric` | body | `string` | no | Metric for contour generation. |
| `contour_style` | body | `string` | no | Style for contour output. |
| `contour_minutes` | body | `string` | no | Travel time for contour generation in minutes. |
| `create_or_update_custom_attributes` | body | `boolean` | no | Whether to create or update custom attributes automatically. |
| `custom_attributes[]` | body | `array<object>` | no | Custom attributes to attach to the location. |
