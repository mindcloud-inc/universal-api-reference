# Generate Product Scene (Fully Generative) with DeepImage

Creates a fully generative product scene in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Generate Product Scene (Fully Generative)](https://documentation.deep-image.ai/common-usecases/create-beautiful-product-photo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the product image to integrate into the generated scene. |
| `background.generate.description` | body | `string` | yes | Prompt describing the fully generated scene. |
| `background.generate.model_type` | body | `string` | no | Generative model used for the scene. |
