# Set Workflow Webhook URL with DocumentPro

Updates a workflow webhook URL in DocumentPro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/templates/:template_id`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Set Workflow Webhook URL](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The workflow template_id. |
| `webhook_url` | body | `string` | yes | The webhook URL to save on the workflow. |
