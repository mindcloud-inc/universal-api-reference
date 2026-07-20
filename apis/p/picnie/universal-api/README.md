# <img src="https://images.mindcloud.co/apps/icons/picnie_1774644402807.png" alt="Picnie logo" width="28" height="28"> Picnie: Universal API

Create, edit, and automate image and PDF assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/picnie/latest
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://picnie.com
- **Vendor API docs:** https://docs.picnie.com/api-reference/api-overview-rl61

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Template](actions/get-template.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=2075" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Upload Asset](actions/upload-asset.md) | POST | Uploads an image asset to Picnie. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Add Image Watermark](actions/add-image-watermark.md) | POST | Creates a watermarked image in Picnie using an image. |
| [Add Text Watermark](actions/add-text-watermark.md) | POST | Creates a watermarked image in Picnie using text. |
| [Apply Image Filter](actions/apply-image-filter.md) | POST | Creates a filtered image in Picnie. |
| [Compress Image](actions/compress-image.md) | POST | Creates a compressed image in Picnie. |
| [Convert Image](actions/convert-image.md) | POST | Creates a converted image in Picnie. |
| [Create Image](actions/create-image.md) | POST | Creates an image in Picnie from a template. |
| [Crop Image](actions/crop-image.md) | POST | Creates a cropped image in Picnie. |
| [Remove Background](actions/remove-background.md) | POST | Creates a background-removed image in Picnie. |
| [Resize Image](actions/resize-image.md) | POST | Creates a resized image in Picnie. |

### Image Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Image Collection](actions/create-image-collection.md) | POST | Creates an image collection in Picnie from a template. |

### Image Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Image Metadata](actions/get-image-metadata.md) | GET | Retrieves JPEG image metadata from Picnie. |

### Image Text

| Action | Method | Description |
| --- | --- | --- |
| [Transcribe Image](actions/transcribe-image.md) | GET | Retrieves OCR text from an image in Picnie. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF](actions/create-pdf.md) | POST | Creates a PDF in Picnie from a template. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Picnie. |
| [List Projects](actions/list-projects.md) | GET | Retrieves your project list from Picnie. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template and its fields from Picnie. |
| [List Templates](actions/list-templates.md) | GET | Retrieves your template list from Picnie. |

