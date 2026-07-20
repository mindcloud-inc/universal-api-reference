# Remove Image Artifacts with WatermarkRemover.io

Removes image artifacts in WatermarkRemover.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/[:cloudName]/[:zone]/af.remove()/[:filePath]`
- **Base URL:** `https://cdn.pixelbin.io`
- **Official documentation:** [Remove Image Artifacts](https://www.pixelbin.io/docs/transformations/ml/artifact-removal/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudName` | path | `string` | no | PixelBin cloud name from the CDN URL. |
| `filePath` | path | `string` | no | Path to the image inside PixelBin storage. |
| `zone` | path | `string` | no | PixelBin zone slug from the CDN URL. |
