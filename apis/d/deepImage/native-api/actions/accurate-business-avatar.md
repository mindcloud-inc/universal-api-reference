# Accurate Business Avatar with DeepImage

Creates an accurate business avatar in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Accurate Business Avatar](https://documentation.deep-image.ai/common-usecases/create-business-photo-or-avatar-from-face-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source face image. |
| `background.generate.description` | body | `string` | yes | Prompt describing the desired accurate business portrait. |
| `background.generate.model_type` | body | `string` | no | Generative model used for avatar creation. |
