# View Hourly Workflow Usage with Natif.ai

Retrieves hourly usage details for a Natif.ai workflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/processing/[:workflowId]/usage/hourly`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [View Hourly Workflow Usage](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_hourly_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow identifier. |
| `start` | query | `string` | yes | Start hour in `%Y-%m-%dT%HZ` format. |
| `end` | query | `string` | no | Optional end hour in `%Y-%m-%dT%HZ` format. Span must be at most one day. |
| `extended` | query | `boolean` | no | Include documents, pages, and average processing time per page. |
