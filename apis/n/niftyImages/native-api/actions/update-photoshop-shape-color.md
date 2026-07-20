# Update Photoshop Shape Color with NiftyImages

Updates a Photoshop shape color in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Psd`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Photoshop Shape Color](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `Layers[]` | body | `array<object>` | yes | PSD layers to update. |
| `Layers[].LayerName` | body | `string` | yes | Layer name. |
| `Layers[].TextColor` | body | `string` | yes | Color value to apply to the layer. |
