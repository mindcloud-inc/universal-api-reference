# Create Styleguide Color with Zeplin

Creates a new styleguide color in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/styleguides/{styleguide_id}/colors`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Styleguide Color](https://docs.zeplin.dev/reference/createstyleguidecolor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `name` | body | `string` | yes | Name of the color |
| `source_id` | body | `string` | yes | Color's identifier in the design tool |
| `r` | body | `number` | yes | Red component of the color |
| `g` | body | `number` | yes | Green component of the color |
| `b` | body | `number` | yes | Blue component of the color |
| `a` | body | `number` | yes | Alpha component of the color |
