# Prepare for Print with DeepImage

Creates a print-ready image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process_result`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Prepare for Print](https://documentation.deep-image.ai/image-processing/print)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the source image to prepare for print. |
| `print_size` | body | `string` | yes | Paper size such as a4, a5, letter, or legal. |
| `dpi` | body | `number` | no | Print DPI. DeepImage defaults this to 300. |
