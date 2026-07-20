# View Monthly Workflow Usage with Natif.ai

Retrieves monthly usage details for a Natif.ai workflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/processing/[:workflowId]/usage/monthly`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [View Monthly Workflow Usage](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_monthly_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow identifier. |
| `start` | query | `string` | yes | Start month in `%Y-%m` format. |
| `end` | query | `string` | no | Optional end month in `%Y-%m` format. Span must be at most one year. |
| `extended` | query | `boolean` | no | Include documents, pages, and average processing time per page. |
