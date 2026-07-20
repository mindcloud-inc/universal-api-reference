# Convert Document with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/convert`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Convert Document](https://docs.docutray.com/docs/operations/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_metadata` | body | `object` | no | Optional metadata returned with the conversion result |
| `document_type_code` | body | `string` | yes | Document type code to use for OCR conversion |
| `image_base64` | body | `string` | no | Base64-encoded image or PDF content |
| `image_content_type` | body | `string` | no | Optional MIME type when Docutray cannot infer it |
| `image_url` | body | `string` | no | HTTP or HTTPS URL of the image or PDF to process |
