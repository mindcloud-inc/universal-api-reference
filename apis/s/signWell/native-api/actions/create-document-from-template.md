# Create Document from Template with SignWell

Creates a new document from a template in SignWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/document_templates/documents`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Create Document from Template](https://developers.signwell.com/reference/post_api-v1-document-templates-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | — |
| `test_mode` | body | `boolean` | no | — |
| `draft` | body | `boolean` | no | Create the document in draft mode so it can be edited and sent later. |
| `embedded_signing` | body | `boolean` | no | — |
| `recipients[]` | body | `array<object>` | yes | — |
| `recipients[].id` | body | `string` | no | — |
| `recipients[].email` | body | `string` | no | — |
| `recipients[].name` | body | `string` | no | — |
| `recipients[].placeholder_name` | body | `string` | no | — |
