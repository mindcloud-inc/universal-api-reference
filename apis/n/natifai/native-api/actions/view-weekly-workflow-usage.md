# View Weekly Workflow Usage with Natif.ai

Retrieves weekly usage details for a Natif.ai workflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/processing/[:workflowId]/usage/weekly`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [View Weekly Workflow Usage](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_weekly_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow identifier. |
| `start` | query | `string` | yes | Start week in `%G-W%V` format. |
| `end` | query | `string` | no | Optional end week in `%G-W%V` format. Span must be at most 6 months. |
| `extended` | query | `boolean` | no | Include documents, pages, and average processing time per page. |
