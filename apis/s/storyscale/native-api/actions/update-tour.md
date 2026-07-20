# Update Tour with Storyscale

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/tour/update/{id}`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Update Tour](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversion_enabled` | body | `boolean` | no | Whether conversion tracking is enabled for the tour. |
| `description` | body | `string` | no | Updated description of the tour. |
| `id` | path | `string` | yes | The Storyscale tour ID. |
| `image` | body | `string` | no | Image for the tour. |
| `is_active` | body | `boolean` | no | Whether the tour is active. |
| `is_published` | body | `boolean` | no | Whether the tour is published. |
| `is_responsive_tour_enabled` | body | `boolean` | no | Whether responsive tour behavior is enabled. |
| `is_template` | body | `boolean` | no | Whether the tour is a template. |
| `name` | body | `string` | no | Updated name of the tour. |
| `style_guide_id` | body | `number` | no | Style guide to associate with the tour. |
