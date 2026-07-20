# List Available Workflows with Natif.ai

Retrieves available processing workflows from Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/processing/workflows`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [List Available Workflows](https://api.natif.ai/docs#/Document%20Capturing/get_available_workflows_processing_workflows_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locale` | query | `string` | no | Locale/language to use for workflow labels. |
| `limit` | query | `number` | no | Maximum number of workflows to return. |
