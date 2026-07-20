# WatermarkRemover.io: Native API Reference

A consolidated summary of WatermarkRemover.io's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.pixelbin.io/docs/api/
- **OpenAPI specification:** https://www.pixelbin.io/docs/api-docs/
- **API base URL:** `https://cdn.pixelbin.io`

## Authentication

### PixelBin API Token and Signature

Authenticates PixelBin API requests with a base64 encoded bearer API token plus PixelBin signature headers.

### Credentials

- **Cloud Name:** `cloudName` · required · PixelBin cloud name used in CDN transformation URLs.
- **Zone:** `zone` · required · PixelBin zone slug used in CDN transformation URLs.

[Official authentication documentation](https://www.pixelbin.io/docs/api/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Object Size](actions/check-object-size.md) | `GET /v2/[:cloudName]/[:zone]/cos.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/check-object-size/) |
| [Check Product Visibility](actions/check-product-visibility.md) | `GET /v2/[:cloudName]/[:zone]/cpv.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/check-product-visibility/) |
| [Count Objects](actions/count-objects.md) | `GET /v2/[:cloudName]/[:zone]/oc.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/object-counter/) |
| [Detect Background Type](actions/detect-background-type.md) | `GET /v2/[:cloudName]/[:zone]/dbt.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/detect-background-type/) |
| [Detect Image Centering](actions/detect-image-centering.md) | `GET /v2/[:cloudName]/[:zone]/imc.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/detect-center/) |
| [Detect NSFW](actions/detect-nsfw.md) | `GET /v2/[:cloudName]/[:zone]/nsfw.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/nsfw-detection/) |
| [Detect Number Plate](actions/detect-number-plate.md) | `GET /v2/[:cloudName]/[:zone]/numPlate.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/detect-number-plate/) |
| [Detect Objects](actions/detect-objects.md) | `GET /v2/[:cloudName]/[:zone]/od.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/object-detection/) |
| [Detect Watermarks](actions/detect-watermarks.md) | `GET /v2/[:cloudName]/[:zone]/wmc.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/detect-watermarks/) |
| [Erase Background](actions/erase-background.md) | `GET /v2/[:cloudName]/[:zone]/erase.bg()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/erase-bg/) |
| [Extract Text](actions/extract-text.md) | `GET /v2/[:cloudName]/[:zone]/ocr.extract()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/extract-text/) |
| [Generate AI Background](actions/generate-ai-background.md) | `GET /v2/[:cloudName]/[:zone]/generate.bg()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/ai-background-generator/) |
| [Generate AI Shadow](actions/generate-ai-shadow.md) | `GET /v2/[:cloudName]/[:zone]/shadow.gen()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/ai-shadow-generator/) |
| [Intelligent Crop](actions/intelligent-crop.md) | `GET /v2/[:cloudName]/[:zone]/ic.crop()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/intelligent-crop/) |
| [Remove Image Artifacts](actions/remove-image-artifacts.md) | `GET /v2/[:cloudName]/[:zone]/af.remove()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/artifact-removal/) |
| [Remove Logo Watermark](actions/remove-logo-watermark.md) | `GET /v2/[:cloudName]/[:zone]/wm.remove(rem_logo\:true)/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/watermark-remover/) |
| [Remove PDF Watermark](actions/remove-pdf-watermark.md) | `GET /v2/[:cloudName]/[:zone]/pwr.remove()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/pdf-watermark-remover/) |
| [Remove Text Watermark](actions/remove-text-watermark.md) | `GET /v2/[:cloudName]/[:zone]/wm.remove(rem_text\:true)/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/watermark-remover/) |
| [Remove Watermark](actions/remove-watermark.md) | `GET /v2/[:cloudName]/[:zone]/wm.remove()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/watermark-remover/) |
| [Remove Watermark In Regions](actions/remove-watermark-in-regions.md) | `GET /v2/[:cloudName]/[:zone]/wm.remove([:regions])/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/watermark-remover/) |
| [Tag Product Image](actions/tag-product-image.md) | `GET /v2/[:cloudName]/[:zone]/apt.tag()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/ai-product-tagging/) |
| [Tag Product View](actions/tag-product-view.md) | `GET /v2/[:cloudName]/[:zone]/vd.detect()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/view-detection/) |
| [Upload Image From URL](actions/upload-image-from-url.md) | `POST https://api.pixelbin.io/service/platform/assets/v1.0/upload/url` | [docs](https://www.pixelbin.io/docs/api/upload-api/) |
| [Upscale Image](actions/upscale-image.md) | `GET /v2/[:cloudName]/[:zone]/sr.upscale()/[:filePath]` | [docs](https://www.pixelbin.io/docs/transformations/ml/upscale/) |
