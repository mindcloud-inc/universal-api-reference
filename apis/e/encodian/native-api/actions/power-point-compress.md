# PowerPoint Compress with Encodian

Compresses a PowerPoint file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PowerPoint/CompressPowerPoint`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PowerPoint Compress](https://support.encodian.com/hc/en-gb/articles/7621965500189)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | The filename of the source file; include the .pptx extension. |
| `fileContent` | body | `string` | yes | The Base64 encoded content of the source PowerPoint file. |
| `compressionRate` | body | `list` | no | Sets the image compression rate; higher values generate smaller files. Accepted values: `0`, `1`, `2`, `3`. |
| `compressEmbeddedFonts` | body | `boolean` | no | Remove unused characters from embedded fonts. |
| `removeUnusedLayoutSlides` | body | `boolean` | no | Remove unused layout slides from the presentation. |
| `removeUnusedMasterSlides` | body | `boolean` | no | Remove unused master slides from the presentation. |
| `resizeImagesToFrameSize` | body | `boolean` | no | Resize images to fit their displayed frames. |
| `cultureName` | body | `string` | no | Culture name used when processing the request. |
