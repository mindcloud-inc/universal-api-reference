# api4ai: Native API Reference

A consolidated summary of api4ai's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://api4.ai/docs
- **API base URL:** `https://api4ai.cloud`

## Authentication

### API Key

Use your API4AI tenant API key. Runtime requests send it in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · optional · Your API4AI tenant API key.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api4.ai/docs)

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Face](actions/analyze-face.md) | `POST /face-analyzer/v1/results` | [docs](https://api4.ai/docs/face-analysis) |
| [Analyze Face from File](actions/analyze-face-from-file.md) | `POST /face-analyzer/v1/results` | [docs](https://api4.ai/docs/face-analysis) |
| [Analyze Fashion](actions/analyze-fashion.md) | `POST /fashion/v2/results` | [docs](https://api4.ai/docs/fashion) |
| [Analyze Fashion from File](actions/analyze-fashion-from-file.md) | `POST /fashion/v2/results` | [docs](https://api4.ai/docs/fashion) |
| [Anonymize Image](actions/anonymize-image.md) | `POST /img-anonymization/v1/results` | [docs](https://api4.ai/docs/image-anonymization) |
| [Anonymize Image from File](actions/anonymize-image-from-file.md) | `POST /img-anonymization/v1/results` | [docs](https://api4.ai/docs/image-anonymization) |
| [Detect Masks](actions/detect-masks.md) | `POST /med-mask/v1/results` | [docs](https://api4.ai/apis/mask-detection) |
| [Detect Masks from File](actions/detect-masks-from-file.md) | `POST /med-mask/v1/results` | [docs](https://api4.ai/apis/mask-detection) |
| [Detect NSFW Content](actions/detect-nsfw-content.md) | `POST /nsfw/v1/results` | [docs](https://api4.ai/docs/nsfw) |
| [Detect NSFW Content from File](actions/detect-nsfw-content-from-file.md) | `POST /nsfw/v1/results` | [docs](https://api4.ai/docs/nsfw) |
| [Detect Objects](actions/detect-objects.md) | `POST /general-det/v1/results` | [docs](https://api4.ai/docs/object-detection) |
| [Detect Objects from File](actions/detect-objects-from-file.md) | `POST /general-det/v1/results` | [docs](https://api4.ai/docs/object-detection) |
| [Extract Text with OCR](actions/extract-text-with-ocr.md) | `POST /ocr/v1/results` | [docs](https://api4.ai/docs/ocr) |
| [Extract Text with OCR from File](actions/extract-text-with-ocr-from-file.md) | `POST /ocr/v1/results` | [docs](https://api4.ai/docs/ocr) |
| [Get Alcohol Recognition API Version](actions/get-alcohol-recognition-api-version.md) | `GET /alco-rec/v1/version` | [docs](https://api4.ai/docs/alco-rec) |
| [Get Background Removal API Version](actions/get-background-removal-api-version.md) | `GET /img-bg-removal/v1/version` | [docs](https://api4.ai/docs/bg-removal) |
| [Get Brand Recognition API Version](actions/get-brand-recognition-api-version.md) | `GET /brand-det/v2/version` | [docs](https://api4.ai/docs/brand-recognition) |
| [Get Face Analysis API Version](actions/get-face-analysis-api-version.md) | `GET /face-analyzer/v1/version` | [docs](https://api4.ai/docs/face-analysis) |
| [Get Fashion API Version](actions/get-fashion-api-version.md) | `GET /fashion/v2/version` | [docs](https://api4.ai/docs/fashion) |
| [Get Household Stuff API Version](actions/get-household-stuff-api-version.md) | `GET /household-stuff/v1/version` | [docs](https://api4.ai/docs/household-stuff) |
| [Get Image Anonymization API Version](actions/get-image-anonymization-api-version.md) | `GET /img-anonymization/v1/version` | [docs](https://api4.ai/docs/image-anonymization) |
| [Get Image Labelling API Version](actions/get-image-labelling-api-version.md) | `GET /general-cls/v1/version` | [docs](https://api4.ai/docs/image-labelling) |
| [Get Image Upscale API Version](actions/get-image-upscale-api-version.md) | `GET /image-upscale/v1/version` | [docs](https://api4.ai/docs/image-upscale) |
| [Get NSFW API Version](actions/get-nsfwapi-version.md) | `GET /nsfw/v1/version` | [docs](https://api4.ai/docs/nsfw) |
| [Get Object Detection API Version](actions/get-object-detection-api-version.md) | `GET /general-det/v1/version` | [docs](https://api4.ai/docs/object-detection) |
| [Get OCR API Version](actions/get-ocrapi-version.md) | `GET /ocr/v1/version` | [docs](https://api4.ai/docs/ocr) |
| [Get Virtual Try-On API Version](actions/get-virtual-try-on-api-version.md) | `GET /virtual-try-on/v1/version` | [docs](https://api4.ai/docs/virtual-try-on) |
| [Get Wine Recognition API Version](actions/get-wine-recognition-api-version.md) | `GET /wine-rec/v1/version` | [docs](https://api4.ai/docs/wine-rec) |
| [Label Image](actions/label-image.md) | `POST /general-cls/v1/results` | [docs](https://api4.ai/docs/image-labelling) |
| [Label Image from File](actions/label-image-from-file.md) | `POST /general-cls/v1/results` | [docs](https://api4.ai/docs/image-labelling) |
| [Recognize Alcohol Content](actions/recognize-alcohol-content.md) | `POST /alco-rec/v1/results` | [docs](https://api4.ai/docs/alco-rec) |
| [Recognize Alcohol Content from File](actions/recognize-alcohol-content-from-file.md) | `POST /alco-rec/v1/results` | [docs](https://api4.ai/docs/alco-rec) |
| [Recognize Brands](actions/recognize-brands.md) | `POST /brand-det/v2/results` | [docs](https://api4.ai/docs/brand-recognition) |
| [Recognize Brands from File](actions/recognize-brands-from-file.md) | `POST /brand-det/v2/results` | [docs](https://api4.ai/docs/brand-recognition) |
| [Recognize Household Stuff](actions/recognize-household-stuff.md) | `POST /household-stuff/v1/results` | [docs](https://api4.ai/docs/household-stuff) |
| [Recognize Household Stuff from File](actions/recognize-household-stuff-from-file.md) | `POST /household-stuff/v1/results` | [docs](https://api4.ai/docs/household-stuff) |
| [Recognize Wine](actions/recognize-wine.md) | `POST /wine-rec/v1/results` | [docs](https://api4.ai/docs/wine-rec) |
| [Recognize Wine from File](actions/recognize-wine-from-file.md) | `POST /wine-rec/v1/results` | [docs](https://api4.ai/docs/wine-rec) |
| [Remove Background](actions/remove-background.md) | `POST /img-bg-removal/v1/results` | [docs](https://api4.ai/docs/bg-removal) |
| [Remove Background from File](actions/remove-background-from-file.md) | `POST /img-bg-removal/v1/results` | [docs](https://api4.ai/docs/bg-removal) |
| [Remove Car Background](actions/remove-car-background.md) | `POST /img-bg-removal/v1/cars/results` | [docs](https://api4.ai/docs/car-bg-removal) |
| [Remove Car Background from File](actions/remove-car-background-from-file.md) | `POST /img-bg-removal/v1/cars/results` | [docs](https://api4.ai/docs/car-bg-removal) |
| [Remove People Background](actions/remove-people-background.md) | `POST /img-bg-removal/v1/people/results` | [docs](https://api4.ai/docs/people-bg-removal) |
| [Remove People Background from File](actions/remove-people-background-from-file.md) | `POST /img-bg-removal/v1/people/results` | [docs](https://api4.ai/docs/people-bg-removal) |
| [Run Virtual Try-On](actions/run-virtual-try-on.md) | `POST /virtual-try-on/v1/results` | [docs](https://api4.ai/docs/virtual-try-on) |
| [Run Virtual Try-On from Files](actions/run-virtual-try-on-from-files.md) | `POST /virtual-try-on/v1/results` | [docs](https://api4.ai/docs/virtual-try-on) |
| [Run Virtual Try-On with Person File and Apparel URL](actions/run-virtual-try-on-with-person-file-and-apparel-url.md) | `POST /virtual-try-on/v1/results` | [docs](https://api4.ai/docs/virtual-try-on) |
| [Run Virtual Try-On with Person URL and Apparel File](actions/run-virtual-try-on-with-person-url-and-apparel-file.md) | `POST /virtual-try-on/v1/results` | [docs](https://api4.ai/docs/virtual-try-on) |
| [Upscale Image](actions/upscale-image.md) | `POST /image-upscale/v1/results` | [docs](https://api4.ai/docs/image-upscale) |
| [Upscale Image from File](actions/upscale-image-from-file.md) | `POST /image-upscale/v1/results` | [docs](https://api4.ai/docs/image-upscale) |
