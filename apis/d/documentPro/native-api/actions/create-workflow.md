# Create Workflow with DocumentPro

Creates a new workflow in DocumentPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/templates`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Create Workflow](https://docs.documentpro.ai/docs/using-api/manage-workflows/create-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parser_config` | body | `object` | no | Parser configuration object for email, OCR, and query settings. |
| `template_schema` | body | `object` | no | Template schema object describing extracted fields. |
| `template_title` | body | `string` | yes | Human-readable title for the workflow. |
| `template_type` | body | `string` | no | Optional workflow type label. |
| `webhook_url` | body | `string` | no | Optional webhook URL for workflow callbacks. |
