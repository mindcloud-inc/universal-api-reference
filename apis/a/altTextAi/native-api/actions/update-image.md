# Update Image with AltText.Ai

Updates an image in your AltText.Ai library.

## Endpoint

- **Method:** `PUT`
- **Path:** `/images/:asset_id`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [Update Image](https://alttext.ai/apidocs#tag/Images/operation/update-image-by-asset-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_id` | path | `string` | yes | The asset ID of the image to update. |
| `image` | body | `object` | yes | The image update payload. Provide fields like `alt_text`, `asset_id`, or `metadata` inside this object. |
| `lang` | query | `string` | no | One or more language codes to update, such as `en` or `en,fr`. |
| `overwrite` | query | `boolean` | no | When true, overwrite existing alt text in the requested language instead of preserving it. |
