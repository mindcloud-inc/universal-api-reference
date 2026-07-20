# Storage-to-Storage Processing with DeepImage

Queues storage-to-storage image processing in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Storage-to-Storage Processing](https://documentation.deep-image.ai/storages/usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | DeepImage storage URL of the source image, for example `storage://aws-deep-image/2025/may/my-photo.png`. |
| `target` | body | `string` | yes | DeepImage storage URL where the processed result should be written. |
