# Set Solid Custom Color with Luxafor

Updates a Luxafor device to a custom solid color.

## Endpoint

- **Method:** `POST`
- **Path:** `/solid_color`
- **Base URL:** `https://api.luxafor.com/webhook/v1/actions`
- **Official documentation:** [Set Solid Custom Color](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionFields` | body | `object` | no | — |
| `actionFields.customColor` | body | `string` | yes | Six-character hexadecimal color code. Use 000000 to turn the device off. |
