# Correct White Balance with DeepImage

Creates an image with corrected white balance in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Correct White Balance](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image whose white balance should be corrected. |
| `white_balance_parameters.level` | body | `number` | no | White balance correction strength from 0.0 to 1.0. |
