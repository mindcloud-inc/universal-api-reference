# <img src="https://images.mindcloud.co/apps/icons/watermark-removerio_1776783198534.png" alt="WatermarkRemover.io logo" width="28" height="28"> WatermarkRemover.io: Universal API

WatermarkRemover.io removes watermarks and related visual artifacts from images using PixelBin-powered transformation APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/watermarkRemoverio/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.watermarkremover.io
- **Vendor API docs:** https://www.pixelbin.io/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Object Size](actions/check-object-size.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/check-object-size?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Check Object Size](actions/check-object-size.md) | GET | Checks object size in a file with WatermarkRemover.io. |
| [Check Product Visibility](actions/check-product-visibility.md) | GET | Checks product visibility in a file with WatermarkRemover.io. |
| [Count Objects](actions/count-objects.md) | GET | Counts objects in a file with WatermarkRemover.io. |
| [Detect Background Type](actions/detect-background-type.md) | GET | Detects background type in a file with WatermarkRemover.io. |
| [Detect Image Centering](actions/detect-image-centering.md) | GET | Detects image centering in a file with WatermarkRemover.io. |
| [Detect NSFW](actions/detect-nsfw.md) | GET | Detects NSFW content in a file with WatermarkRemover.io. |
| [Detect Number Plate](actions/detect-number-plate.md) | GET | Detects a number plate in a file with WatermarkRemover.io. |
| [Detect Objects](actions/detect-objects.md) | GET | Detects objects in a file with WatermarkRemover.io. |
| [Detect Watermarks](actions/detect-watermarks.md) | GET | Detects watermarks in a file with WatermarkRemover.io. |
| [Erase Background](actions/erase-background.md) | GET | Erases a file background in WatermarkRemover.io. |
| [Extract Text](actions/extract-text.md) | GET | Extracts text from a file with WatermarkRemover.io. |
| [Generate AI Background](actions/generate-ai-background.md) | GET | Generates an AI background for a file in WatermarkRemover.io. |
| [Generate AI Shadow](actions/generate-ai-shadow.md) | GET | Generates an AI shadow for a file in WatermarkRemover.io. |
| [Intelligent Crop](actions/intelligent-crop.md) | GET | Crops a file intelligently in WatermarkRemover.io. |
| [Remove Image Artifacts](actions/remove-image-artifacts.md) | GET | Removes image artifacts in WatermarkRemover.io. |
| [Remove Logo Watermark](actions/remove-logo-watermark.md) | GET | Removes logo watermarks from a file in WatermarkRemover.io. |
| [Remove PDF Watermark](actions/remove-pdf-watermark.md) | GET | Removes a watermark from a PDF in WatermarkRemover.io. |
| [Remove Text Watermark](actions/remove-text-watermark.md) | GET | Removes text watermarks from a file in WatermarkRemover.io. |
| [Remove Watermark](actions/remove-watermark.md) | GET | Removes a watermark from a file in WatermarkRemover.io. |
| [Remove Watermark In Regions](actions/remove-watermark-in-regions.md) | GET | Removes watermarks from selected regions in WatermarkRemover.io. |
| [Tag Product Image](actions/tag-product-image.md) | GET | Tags a product image with WatermarkRemover.io. |
| [Tag Product View](actions/tag-product-view.md) | GET | Tags a product view with WatermarkRemover.io. |
| [Upload Image From URL](actions/upload-image-from-url.md) | POST | Uploads an image to WatermarkRemover.io from a URL. |
| [Upscale Image](actions/upscale-image.md) | GET | Upscales an image in WatermarkRemover.io. |

