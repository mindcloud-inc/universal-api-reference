# Detect Watermarks with WatermarkRemover.io

Detects watermarks in a file with WatermarkRemover.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/[:cloudName]/[:zone]/wmc.detect()/[:filePath]`
- **Base URL:** `https://cdn.pixelbin.io`
- **Official documentation:** [Detect Watermarks](https://www.pixelbin.io/docs/transformations/ml/detect-watermarks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudName` | path | `string` | no | PixelBin cloud name from the CDN URL. |
| `filePath` | path | `string` | no | Path to the image inside PixelBin storage. |
| `zone` | path | `string` | no | PixelBin zone slug from the CDN URL. |
