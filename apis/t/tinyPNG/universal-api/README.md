# <img src="https://images.mindcloud.co/apps/icons/tinify-icon_1775487617376.png" alt="TinyPNG logo" width="28" height="28"> TinyPNG: Universal API

Optimize images with TinyPNG's Tinify API using compression, resizing, conversion, metadata preservation, and direct cloud storage outputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tinyPNG/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tinify.com
- **Vendor API docs:** https://tinify.com/developers/reference/http

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Optimized Image](actions/download-optimized-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/download-optimized-image?connectionId=$CONNECTION_ID&outputPath=%2Foutput%2Fabc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Compress Image From URL](actions/compress-image-from-url.md) | POST | Compresses an image from a URL with TinyPNG. |
| [Convert Image To AVIF](actions/convert-image-to-avif.md) | POST | Creates an AVIF image from TinyPNG output. |
| [Convert Image To JPEG Black Background](actions/convert-image-to-jpeg-black-background.md) | POST | Creates a JPEG image with a black background in TinyPNG. |
| [Convert Image To JPEG White Background](actions/convert-image-to-jpeg-white-background.md) | POST | Creates a JPEG image with a white background in TinyPNG. |
| [Convert Image To PNG](actions/convert-image-to-png.md) | POST | Creates a PNG image from TinyPNG output. |
| [Convert Image To Smallest Supported Format](actions/convert-image-to-smallest-supported-format.md) | POST | Creates the smallest supported image format in TinyPNG. |
| [Convert Image To WebP](actions/convert-image-to-web-p.md) | POST | Creates a WebP image from TinyPNG output. |
| [Download Optimized Image](actions/download-optimized-image.md) | GET | Downloads an optimized image from TinyPNG. |
| [Preserve Copyright And Creation Metadata](actions/preserve-copyright-and-creation-metadata.md) | PUT | Preserves copyright and creation metadata in TinyPNG output. |
| [Preserve Copyright Metadata](actions/preserve-copyright-metadata.md) | PUT | Preserves copyright metadata in TinyPNG output. |
| [Preserve Creation Metadata](actions/preserve-creation-metadata.md) | PUT | Preserves creation metadata in TinyPNG output. |
| [Preserve Location Metadata](actions/preserve-location-metadata.md) | PUT | Preserves location metadata in TinyPNG output. |
| [Resize Image Cover Custom](actions/resize-image-cover-custom.md) | POST | Creates a TinyPNG image resized with custom cover dimensions. |
| [Resize Image Cover 300x300](actions/resize-image-cover300x300.md) | POST | Creates a TinyPNG image resized to cover 300x300. |
| [Resize Image Fit Custom](actions/resize-image-fit-custom.md) | POST | Creates a TinyPNG image resized with custom fit dimensions. |
| [Resize Image Fit 150x100](actions/resize-image-fit150x100.md) | POST | Creates a TinyPNG image resized to fit 150x100. |
| [Resize Image Fit 300x200](actions/resize-image-fit300x200.md) | POST | Creates a TinyPNG image resized to fit 300x200. |
| [Resize Image Scale Custom](actions/resize-image-scale-custom.md) | POST | Creates a TinyPNG image scaled to a custom size. |
| [Resize Image Scale To Height 150](actions/resize-image-scale-to-height150.md) | POST | Creates a TinyPNG image scaled to height 150. |
| [Resize Image Scale To Height 300](actions/resize-image-scale-to-height300.md) | POST | Creates a TinyPNG image scaled to height 300. |
| [Resize Image Scale To Height 600](actions/resize-image-scale-to-height600.md) | POST | Creates a TinyPNG image scaled to height 600. |
| [Resize Image Scale To Height 64](actions/resize-image-scale-to-height64.md) | POST | Creates a TinyPNG image scaled to height 64. |
| [Resize Image Scale To Width 150](actions/resize-image-scale-to-width150.md) | POST | Creates a TinyPNG image scaled to width 150. |
| [Resize Image Scale To Width 300](actions/resize-image-scale-to-width300.md) | POST | Creates a TinyPNG image scaled to width 300. |
| [Resize Image Scale To Width 600](actions/resize-image-scale-to-width600.md) | POST | Creates a TinyPNG image scaled to width 600. |
| [Resize Image Scale To Width 64](actions/resize-image-scale-to-width64.md) | POST | Creates a TinyPNG image scaled to width 64. |
| [Resize Image Thumb Custom](actions/resize-image-thumb-custom.md) | POST | Creates a TinyPNG thumbnail with custom dimensions. |
| [Resize Image Thumb 150x150](actions/resize-image-thumb150x150.md) | POST | Creates a TinyPNG thumbnail resized to 150x150. |
| [Store Image To Amazon S3](actions/store-image-to-amazon-s3.md) | POST | Stores a TinyPNG image in Amazon S3. |
| [Store Image To Google Cloud Storage](actions/store-image-to-google-cloud-storage.md) | POST | Stores a TinyPNG image in Google Cloud Storage. |

