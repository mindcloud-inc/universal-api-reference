# Adjust Image with Picsart

Creates an adjusted image in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/adjust`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Adjust Image](https://docs.picsart.io/reference/image-adjust)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `brightness` | body | `number` | no | Adjust brightness from -100 to 100. |
| `contrast` | body | `number` | no | Adjust contrast from -100 to 100. |
| `saturation` | body | `number` | no | Adjust saturation from -100 to 100. |
| `format` | body | `string` | no | Optional output image format. |
