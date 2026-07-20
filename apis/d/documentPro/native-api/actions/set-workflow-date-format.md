# Set Workflow Date Format with DocumentPro

Updates the date format for a DocumentPro workflow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/templates/:template_id`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Set Workflow Date Format](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parser_config.date_format` | body | `string` | yes | The date format string to apply, for example %Y-%m-%d. |
| `template_id` | path | `string` | yes | The workflow template_id. |
