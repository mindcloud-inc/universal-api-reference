# Create Template with PDFMonkey

Creates a template in PDFMonkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/document_templates`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [Create Template](https://pdfmonkey.io/docs/api/templates/#create-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | Human name of the document template. |
| `edition_mode` | body | `string` | no | Template editing mode. |
| `body_draft` | body | `string` | no | Draft HTML + Liquid content. |
| `scss_style_draft` | body | `string` | no | Draft CSS or SCSS style. |
| `sample_data_draft` | body | `string` | no | Draft sample data as a JSON string. |
| `settings_draft` | body | `object` | no | Draft template settings object. |
| `pdf_engine_draft_id` | body | `string` | yes | PDF engine used to preview draft changes. |
| `ttl` | body | `number` | no | Document expiration delay in seconds. |
