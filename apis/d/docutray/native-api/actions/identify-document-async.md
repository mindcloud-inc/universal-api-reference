# Start Document Identification with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/identify-async`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Start Document Identification](https://docs.docutray.com/docs/operations/identify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_metadata` | body | `object` | no | Optional metadata returned with the identification result |
| `document_type_code_options[]` | body | `array<string>` | yes | Document type codes to consider during identification |
| `image_base64` | body | `string` | no | Base64-encoded image or PDF content |
| `image_content_type` | body | `string` | no | Optional MIME type when Docutray cannot infer it |
| `image_url` | body | `string` | no | HTTP or HTTPS URL of the image or PDF to identify |
