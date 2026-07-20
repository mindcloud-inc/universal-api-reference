# Encodian - Image: Native API Reference

A consolidated summary of Encodian - Image's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-gb/connectors/encodianimage/
- **OpenAPI specification:** https://api.apps-encodian.com/swagger/Image/swagger.json
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Authenticate requests to Encodian Flowr Image with the X-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-gb/connectors/encodianimage/#creating-a-connection)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Image - Add Image Watermark](actions/image-add-image-watermark.md) | `POST /api/v1/Image/AddImageWatermarkToImage` | [docs](https://support.encodian.com/hc/en-gb/articles/8967068141597) |
| [Image - Add Text Watermark](actions/image-add-text-watermark.md) | `POST /api/v1/Image/AddTextWatermarkToImage` | [docs](https://support.encodian.com/hc/en-gb/articles/360013560398-Add-Text-Watermark-To-Image) |
| [Image - Clean Up Document](actions/image-clean-up-document.md) | `POST /api/v1/Image/ImageCleanUpDocument` | [docs](https://learn.microsoft.com/en-gb/connectors/encodianimage/#image---clean-up-document) |
| [Image - Clean Up Photo](actions/image-clean-up-photo.md) | `POST /api/v1/Image/ImageCleanUpPhoto` | [docs](https://learn.microsoft.com/en-gb/connectors/encodianimage/#image---clean-up-photo) |
| [Image - Compress](actions/image-compress.md) | `POST /api/v1/Image/CompressImage` | [docs](https://support.encodian.com/hc/en-gb/articles/360027350513-Compress-an-Image) |
| [Image - Convert Format](actions/image-convert-format.md) | `POST /api/v1/Image/ImageConvertFormat` | [docs](https://support.encodian.com/hc/en-gb/articles/360006617857-Convert-Image-Format) |
| [Image - Convert to Grayscale](actions/image-convert-to-grayscale.md) | `POST /api/v1/Image/ImageConvertToGrayscale` | [docs](https://learn.microsoft.com/en-gb/connectors/encodianimage/#image---convert-to-grayscale) |
| [Image - Crop](actions/image-crop.md) | `POST /api/v1/Image/CropImage` | [docs](https://support.encodian.com/hc/en-gb/articles/10860483459740/) |
| [Image - Extract Metadata](actions/image-extract-metadata.md) | `POST /api/v1/Image/GetImageInfo` | [docs](https://support.encodian.com/hc/en-gb/articles/4431662425489) |
| [Image - Extract Text](actions/image-extract-text.md) | `POST /api/v1/Image/ImageExtractText` | [docs](https://support.encodian.com/hc/en-gb/articles/360006998078-Extract-Text-from-Image-OCR) |
| [Image - Flip](actions/image-flip.md) | `POST /api/v1/Image/FlipImage` | [docs](https://support.encodian.com/hc/en-gb/articles/9798473339292) |
| [Image - Remove EXIF Tags](actions/image-remove-exif-tags.md) | `POST /api/v1/Image/ImageRemoveExifTags` | [docs](https://support.encodian.com/hc/en-gb/articles/4415700524817) |
| [Image - Resize](actions/image-resize.md) | `POST /api/v1/Image/ResizeImage` | [docs](https://support.encodian.com/hc/en-gb/articles/360018591034-Resize-an-Image) |
| [Image - Rotate](actions/image-rotate.md) | `POST /api/v1/Image/RotateImage` | [docs](https://support.encodian.com/hc/en-gb/articles/10041551840796) |
| [Image - Rotate by EXIF Data](actions/image-rotate-by-exif-data.md) | `POST /api/v1/Image/RotateImageByExifData` | [docs](https://support.encodian.com/hc/en-gb/articles/16556447851804) |
