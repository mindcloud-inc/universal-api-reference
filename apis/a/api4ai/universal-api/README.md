# <img src="https://images.mindcloud.co/apps/icons/api4ai-icon_1776189026038.png" alt="api4ai logo" width="28" height="28"> api4ai: Universal API

API4AI provides computer vision and image-processing APIs for OCR, object detection, face analysis, background removal, brand recognition, image labelling, NSFW detection, virtual try-on, and related media analysis workloads.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/api4ai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://api4.ai
- **Vendor API docs:** https://api4.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get OCR API Version](actions/get-ocrapi-version.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/get-ocrapi-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Alcohol Recognition Result

| Action | Method | Description |
| --- | --- | --- |
| [Recognize Alcohol Content](actions/recognize-alcohol-content.md) | GET | Recognizes alcohol labels from an image URL in api4ai. |
| [Recognize Alcohol Content from File](actions/recognize-alcohol-content-from-file.md) | GET | Recognizes alcohol labels from an image file in api4ai. |

### Api Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Alcohol Recognition API Version](actions/get-alcohol-recognition-api-version.md) | GET | Retrieves the alcohol recognition API version from api4ai. |
| [Get Background Removal API Version](actions/get-background-removal-api-version.md) | GET | Retrieves the background removal API version from api4ai. |
| [Get Brand Recognition API Version](actions/get-brand-recognition-api-version.md) | GET | Retrieves the brand recognition API version from api4ai. |
| [Get Face Analysis API Version](actions/get-face-analysis-api-version.md) | GET | Retrieves the face analysis API version from api4ai. |
| [Get Fashion API Version](actions/get-fashion-api-version.md) | GET | Retrieves the fashion API version from api4ai. |
| [Get Household Stuff API Version](actions/get-household-stuff-api-version.md) | GET | Retrieves the household stuff API version from api4ai. |
| [Get Image Anonymization API Version](actions/get-image-anonymization-api-version.md) | GET | Retrieves the image anonymization API version from api4ai. |
| [Get Image Labelling API Version](actions/get-image-labelling-api-version.md) | GET | Retrieves the image labelling API version from api4ai. |
| [Get Image Upscale API Version](actions/get-image-upscale-api-version.md) | GET | Retrieves the image upscale API version from api4ai. |
| [Get NSFW API Version](actions/get-nsfwapi-version.md) | GET | Retrieves the NSFW API version from api4ai. |
| [Get Object Detection API Version](actions/get-object-detection-api-version.md) | GET | Retrieves the object detection API version from api4ai. |
| [Get OCR API Version](actions/get-ocrapi-version.md) | GET | Retrieves the OCR API version from api4ai. |
| [Get Virtual Try-On API Version](actions/get-virtual-try-on-api-version.md) | GET | Retrieves the virtual try-on API version from api4ai. |
| [Get Wine Recognition API Version](actions/get-wine-recognition-api-version.md) | GET | Retrieves the wine recognition API version from api4ai. |

### Background Removal Result

| Action | Method | Description |
| --- | --- | --- |
| [Remove Background](actions/remove-background.md) | GET | Removes an image background from a URL in api4ai. |
| [Remove Background from File](actions/remove-background-from-file.md) | GET | Removes an image background from a file in api4ai. |

### Brand Recognition Result

| Action | Method | Description |
| --- | --- | --- |
| [Recognize Brands](actions/recognize-brands.md) | GET | Recognizes brands from an image URL in api4ai. |
| [Recognize Brands from File](actions/recognize-brands-from-file.md) | GET | Recognizes brands from an image file in api4ai. |

### Car Background Removal Result

| Action | Method | Description |
| --- | --- | --- |
| [Remove Car Background](actions/remove-car-background.md) | GET | Removes a car background from a URL in api4ai. |
| [Remove Car Background from File](actions/remove-car-background-from-file.md) | GET | Removes a car background from a file in api4ai. |

### Face Analysis Result

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Face](actions/analyze-face.md) | GET | Analyzes a face from an image URL in api4ai. |
| [Analyze Face from File](actions/analyze-face-from-file.md) | GET | Analyzes a face from an image file in api4ai. |

### Fashion Analysis Result

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Fashion](actions/analyze-fashion.md) | GET | Analyzes fashion items from an image URL in api4ai. |
| [Analyze Fashion from File](actions/analyze-fashion-from-file.md) | GET | Analyzes fashion items from an image file in api4ai. |

### Household Stuff Recognition Result

| Action | Method | Description |
| --- | --- | --- |
| [Recognize Household Stuff](actions/recognize-household-stuff.md) | GET | Recognizes household items from an image URL in api4ai. |
| [Recognize Household Stuff from File](actions/recognize-household-stuff-from-file.md) | GET | Recognizes household items from an image file in api4ai. |

### Image Anonymization Result

| Action | Method | Description |
| --- | --- | --- |
| [Anonymize Image](actions/anonymize-image.md) | GET | Anonymizes an image from a URL in api4ai. |
| [Anonymize Image from File](actions/anonymize-image-from-file.md) | GET | Anonymizes an image from a file in api4ai. |

### Image Labelling Result

| Action | Method | Description |
| --- | --- | --- |
| [Label Image](actions/label-image.md) | GET | Labels an image from a URL in api4ai. |
| [Label Image from File](actions/label-image-from-file.md) | GET | Labels an image from a file in api4ai. |

### Image Upscale Result

| Action | Method | Description |
| --- | --- | --- |
| [Upscale Image](actions/upscale-image.md) | GET | Upscales an image from a URL in api4ai. |
| [Upscale Image from File](actions/upscale-image-from-file.md) | GET | Upscales an image from a file in api4ai. |

### Mask Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect Masks](actions/detect-masks.md) | GET | Detects face masks from an image URL in api4ai. |
| [Detect Masks from File](actions/detect-masks-from-file.md) | GET | Detects face masks from an image file in api4ai. |

### Nsfw Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect NSFW Content](actions/detect-nsfw-content.md) | GET | Detects NSFW content from an image URL in api4ai. |
| [Detect NSFW Content from File](actions/detect-nsfw-content-from-file.md) | GET | Detects NSFW content from an image file in api4ai. |

### Object Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect Objects](actions/detect-objects.md) | GET | Detects objects from an image URL in api4ai. |
| [Detect Objects from File](actions/detect-objects-from-file.md) | GET | Detects objects from an image file in api4ai. |

### Ocr Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Text with OCR](actions/extract-text-with-ocr.md) | GET | Extracts text from an image URL in api4ai. |
| [Extract Text with OCR from File](actions/extract-text-with-ocr-from-file.md) | GET | Extracts text from an image file in api4ai. |

### People Background Removal Result

| Action | Method | Description |
| --- | --- | --- |
| [Remove People Background](actions/remove-people-background.md) | GET | Removes a person's background from a URL in api4ai. |
| [Remove People Background from File](actions/remove-people-background-from-file.md) | GET | Removes a person's background from a file in api4ai. |

### Virtual Try-on Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Virtual Try-On](actions/run-virtual-try-on.md) | GET | Runs virtual try-on from person and apparel URLs in api4ai. |
| [Run Virtual Try-On from Files](actions/run-virtual-try-on-from-files.md) | GET | Runs virtual try-on from person and apparel files in api4ai. |
| [Run Virtual Try-On with Person File and Apparel URL](actions/run-virtual-try-on-with-person-file-and-apparel-url.md) | GET | Runs virtual try-on from a person file and apparel URL in api4ai. |
| [Run Virtual Try-On with Person URL and Apparel File](actions/run-virtual-try-on-with-person-url-and-apparel-file.md) | GET | Runs virtual try-on from a person URL and apparel file in api4ai. |

### Wine Recognition Result

| Action | Method | Description |
| --- | --- | --- |
| [Recognize Wine](actions/recognize-wine.md) | GET | Recognizes wine labels from an image URL in api4ai. |
| [Recognize Wine from File](actions/recognize-wine-from-file.md) | GET | Recognizes wine labels from an image file in api4ai. |

