# Count Objects with WatermarkRemover.io

Counts objects in a file with WatermarkRemover.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/[:cloudName]/[:zone]/oc.detect()/[:filePath]`
- **Base URL:** `https://cdn.pixelbin.io`
- **Official documentation:** [Count Objects](https://www.pixelbin.io/docs/transformations/ml/object-counter/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudName` | path | `string` | no | PixelBin cloud name from the CDN URL. |
| `filePath` | path | `string` | no | Path to the image inside PixelBin storage. |
| `zone` | path | `string` | no | PixelBin zone slug from the CDN URL. |
