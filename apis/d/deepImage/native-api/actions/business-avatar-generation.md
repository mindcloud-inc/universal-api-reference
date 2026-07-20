# Business Avatar Generation with DeepImage

Creates a business avatar image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Business Avatar Generation](https://documentation.deep-image.ai/common-usecases/create-business-photo-or-avatar-from-face-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source face image. |
| `background.generate.description` | body | `string` | yes | Prompt describing the desired business portrait or avatar. |
| `background.generate.face_id` | body | `boolean` | no | When enabled, DeepImage uses the documented `face_id` toggle to allow more changes to hair and similar details. |
