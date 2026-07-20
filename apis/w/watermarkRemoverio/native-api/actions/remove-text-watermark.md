# Remove Text Watermark with WatermarkRemover.io

Removes text watermarks from a file in WatermarkRemover.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/[:cloudName]/[:zone]/wm.remove(rem_text\:true)/[:filePath]`
- **Base URL:** `https://cdn.pixelbin.io`
- **Official documentation:** [Remove Text Watermark](https://www.pixelbin.io/docs/transformations/ml/watermark-remover/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudName` | path | `string` | no | PixelBin cloud name from the CDN URL. |
| `filePath` | path | `string` | no | Path to the image inside PixelBin storage. |
| `zone` | path | `string` | no | PixelBin zone slug from the CDN URL. |
