# Update Template with PDFMonkey

Updates an existing template in PDFMonkey.

## Endpoint

- **Method:** `PUT`
- **Path:** `/document_templates/:id`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [Update Template](https://pdfmonkey.io/docs/api/templates/#update-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the template to update. |
| `identifier` | body | `string` | no | Human name of the document template. |
| `edition_mode` | body | `string` | no | Template editing mode. |
| `body_draft` | body | `string` | no | Draft HTML + Liquid content. |
| `scss_style_draft` | body | `string` | no | Draft CSS or SCSS style. |
| `sample_data_draft` | body | `string` | no | Draft sample data as a JSON string. |
| `settings_draft` | body | `object` | no | Draft template settings object. |
| `pdf_engine_draft_id` | body | `string` | yes | PDF engine used to preview draft changes. |
| `ttl` | body | `number` | no | Document expiration delay in seconds. |
