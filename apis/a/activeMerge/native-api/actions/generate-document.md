# Generate Document with ActiveMerge

Generates a document from a template in ActiveMerge.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/document-generation/generate`
- **Base URL:** `https://app.activemerge.com`
- **Official documentation:** [Generate Document](https://app.activemerge.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Object mapping template placeholders to values. |
| `format` | body | `string` | yes | Output format: pdf, docx, or pptx. Accepted values: `0`, `1`, `2`. |
| `template_id` | body | `string` | yes | Template ID to use for document generation. |
