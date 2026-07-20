# Update a Workflow with DocuPanda - Document Understanding

Updates an existing workflow in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/:workflow_id/update`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update a Workflow](https://docs.docupipe.ai/reference/update_workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classifyStandardizeStep` | body | `object` | no | — |
| `splitClassifyStandardizeStep` | body | `object` | no | — |
| `splitStandardizeStep` | body | `object` | no | — |
| `standardizeReviewStep` | body | `object` | no | — |
| `standardizeStep` | body | `object` | no | — |
| `workflow_id` | path | `string` | yes | — |
| `workflowName` | body | `string` | no | Optionally name your workflow |
