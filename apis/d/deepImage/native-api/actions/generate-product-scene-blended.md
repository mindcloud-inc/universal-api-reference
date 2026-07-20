# Generate Product Scene (Blended) with DeepImage

Creates a blended product scene in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Generate Product Scene (Blended)](https://documentation.deep-image.ai/common-usecases/create-beautiful-product-photo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the product image to place into the generated scene. |
| `background.generate.description` | body | `string` | yes | Prompt describing the target scene around the product. |
| `background.generate.item_area_percentage` | body | `number` | no | Value between 0 and 1 controlling how much of the image the product should occupy. |
| `width` | body | `number` | no | Optional output width in pixels. |
| `height` | body | `number` | no | Optional output height in pixels. |
