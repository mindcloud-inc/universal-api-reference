# Update Photoshop Smart Object Image with NiftyImages

Updates a Photoshop smart object image in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Psd`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Photoshop Smart Object Image](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `Layers[]` | body | `array<object>` | yes | PSD layers to update. |
| `Layers[].LayerName` | body | `string` | yes | Layer name. |
| `Layers[].ImageUrl` | body | `string` | yes | Image URL to place into the smart object layer. |
