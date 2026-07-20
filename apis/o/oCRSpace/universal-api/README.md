# <img src="https://images.mindcloud.co/apps/icons/o-crspace_1775769139837.png" alt="OCRSpace logo" width="28" height="28"> OCRSpace: Universal API

OCRSpace: Extract text from images and PDFs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oCRSpace/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ocr.space/
- **Vendor API docs:** https://ocr.space/ocrapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Parse Image URL](actions/parse-image-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/parse-image-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Searchable PDF From File](actions/create-searchable-pdf-from-file.md) | GET |  |
| [Extract Tables From File](actions/extract-tables-from-file.md) | GET |  |
| [Recognize Layout From File](actions/recognize-layout-from-file.md) | GET |  |
| [Upload File With Overlay](actions/upload-file-with-overlay.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Searchable PDF From Base64](actions/create-searchable-pdf-from-base64.md) | GET |  |
| [Create Searchable PDF From URL](actions/create-searchable-pdf-from-url.md) | GET |  |
| [Detect Language From URL](actions/detect-language-from-url.md) | GET |  |
| [Extract Tables From Base64](actions/extract-tables-from-base64.md) | GET |  |
| [Extract Tables From URL](actions/extract-tables-from-url.md) | GET |  |
| [Parse Base64 Document](actions/parse-base64-document.md) | GET |  |
| [Parse Base64 With Overlay](actions/parse-base64-with-overlay.md) | GET |  |
| [Parse Image URL](actions/parse-image-url.md) | GET |  |
| [Parse Image URL With Overlay](actions/parse-image-url-with-overlay.md) | GET |  |
| [Parse URL Securely](actions/parse-url-securely.md) | GET |  |
| [Recognize Layout From Base64](actions/recognize-layout-from-base64.md) | GET |  |
| [Recognize Layout From URL](actions/recognize-layout-from-url.md) | GET |  |
| [Upload File For OCR](actions/upload-file-for-ocr.md) | GET |  |

