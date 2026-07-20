# Update Photoshop Image Layers with NiftyImages

Updates Photoshop image layers in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Psd`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Photoshop Image Layers](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `Name` | body | `string` | no | Name of the image. |
| `Variables[]` | body | `array<object>` | no | Variables array. |
| `Variables[].Name` | body | `string` | no | Variable or placeholder name. |
| `Variables[].DefaultValue` | body | `string` | no | Default value for the variable. |
| `Layers[]` | body | `array<object>` | yes | PSD layers to update. |
| `Layers[].LayerName` | body | `string` | yes | Layer name. |
| `Layers[].TextValue` | body | `string` | no | Text value to apply to the layer. |
| `Layers[].TextColor` | body | `string` | no | Color to apply to the layer. |
| `Layers[].ImageUrl` | body | `string` | no | Image URL for smart object layer updates. |
| `Layers[].Show` | body | `boolean` | no | Set to true to show the layer or false to hide it. |
