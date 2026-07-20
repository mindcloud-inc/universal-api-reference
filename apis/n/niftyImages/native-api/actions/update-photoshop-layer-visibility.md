# Update Photoshop Layer Visibility with NiftyImages

Updates Photoshop layer visibility in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Psd`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Photoshop Layer Visibility](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `Layers[]` | body | `array<object>` | yes | PSD layers to update. |
| `Layers[].LayerName` | body | `string` | yes | Layer name. |
| `Layers[].Show` | body | `boolean` | yes | Set to true to show the layer or false to hide it. |
