# Update Workflow with DocumentPro

Updates an existing workflow in DocumentPro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/templates/:template_id`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Update Workflow](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parser_config` | body | `object` | no | Updated parser configuration object. |
| `template_id` | path | `string` | yes | The workflow template_id. |
| `template_schema` | body | `object` | no | Updated template schema object. |
| `template_title` | body | `string` | no | Updated workflow title. |
| `template_type` | body | `string` | no | Updated workflow type. |
| `webhook_url` | body | `string` | no | Updated webhook URL. |
