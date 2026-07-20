# Remove Watermark In Regions with WatermarkRemover.io

Removes watermarks from selected regions in WatermarkRemover.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/[:cloudName]/[:zone]/wm.remove([:regions])/[:filePath]`
- **Base URL:** `https://cdn.pixelbin.io`
- **Official documentation:** [Remove Watermark In Regions](https://www.pixelbin.io/docs/transformations/ml/watermark-remover/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudName` | path | `string` | no | PixelBin cloud name from the CDN URL. |
| `filePath` | path | `string` | no | Path to the image inside PixelBin storage. |
| `regions` | path | `string` | no | Watermark removal region parameters for up to five boxes, formatted for the PixelBin wm.remove transformation. |
| `zone` | path | `string` | no | PixelBin zone slug from the CDN URL. |
