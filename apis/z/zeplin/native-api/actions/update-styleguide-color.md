# Update Styleguide Color with Zeplin

Updates an existing styleguide color in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/styleguides/{styleguide_id}/colors/{color_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Styleguide Color](https://docs.zeplin.dev/reference/updatestyleguidecolor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `color_id` | path | `string` | yes | Color id |
| `name` | body | `string` | yes | Name of the color |
| `r` | body | `number` | yes | Red component of the color |
| `g` | body | `number` | yes | Green component of the color |
| `b` | body | `number` | yes | Blue component of the color |
| `a` | body | `number` | yes | Alpha component of the color |
