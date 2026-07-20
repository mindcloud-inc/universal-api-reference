# View Daily Workflow Usage with Natif.ai

Retrieves daily usage details for a Natif.ai workflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/processing/[:workflowId]/usage/daily`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [View Daily Workflow Usage](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_daily_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow identifier. |
| `start` | query | `string` | yes | Start date in `%Y-%m-%d` format. |
| `end` | query | `string` | no | Optional end date in `%Y-%m-%d` format. Span must be at most 30 days. |
| `extended` | query | `boolean` | no | Include documents, pages, and average processing time per page. |
