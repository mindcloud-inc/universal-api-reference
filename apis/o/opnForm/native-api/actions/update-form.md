# Update Form with OpnForm

Updates an existing form in OpnForm.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open/forms/:id`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Update Form](https://docs.opnform.com/api-reference/forms/update-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric ID of the form to update. |
| `title` | body | `string` | yes | Human-readable form title. |
| `visibility` | body | `string` | yes | Form visibility state. |
| `language` | body | `string` | yes | Two-letter ISO language code. |
| `theme` | body | `string` | yes | Form theme. |
| `presentation_style` | body | `string` | yes | Form presentation style. |
| `width` | body | `string` | yes | Form width. |
| `size` | body | `string` | yes | Form size. |
| `border_radius` | body | `string` | yes | Form border radius. |
| `dark_mode` | body | `string` | yes | Dark mode setting. |
| `color` | body | `string` | yes | Primary color in hex format. |
| `uppercase_labels` | body | `boolean` | yes | Whether labels should be uppercase. |
| `no_branding` | body | `boolean` | yes | Whether to hide OpnForm branding. |
| `transparent_background` | body | `boolean` | yes | Whether to use a transparent background. |
| `properties` | body | `object` | yes | Complete JSON array of form blocks and fields. Do not send an empty array. |
