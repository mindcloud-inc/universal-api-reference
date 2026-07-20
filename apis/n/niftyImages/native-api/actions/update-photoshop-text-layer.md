# Update Photoshop Text Layer with NiftyImages

Updates a Photoshop text layer in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Psd`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Photoshop Text Layer](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `Layers[]` | body | `array<object>` | yes | PSD layers to update. |
| `Layers[].LayerName` | body | `string` | yes | Layer name. |
| `Layers[].TextValue` | body | `string` | yes | Text value to apply to the layer. |
| `Layers[].TextColor` | body | `string` | no | Optional text color for the layer. |
