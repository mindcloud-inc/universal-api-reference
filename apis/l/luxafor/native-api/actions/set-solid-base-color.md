# Set Solid Base Color with Luxafor

Updates a Luxafor device to a preset solid color.

## Endpoint

- **Method:** `POST`
- **Path:** `/solid_color`
- **Base URL:** `https://api.luxafor.com/webhook/v1/actions`
- **Official documentation:** [Set Solid Base Color](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionFields` | body | `object` | no | — |
| `actionFields.color` | body | `string` | yes | Accepted colors: red, green, yellow, blue, white, cyan, magenta. |
