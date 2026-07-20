# Create a Workflow with DocuPanda - Document Understanding

Creates an on-submit workflow in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/on-submit-document`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Create a Workflow](https://docs.docupipe.ai/reference/post_workflow_on_submit_document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classifyStandardizeStep` | body | `object` | no | — |
| `splitClassifyStandardizeStep` | body | `object` | no | — |
| `splitStandardizeStep` | body | `object` | no | — |
| `standardizeReviewStep` | body | `object` | no | — |
| `standardizeStep` | body | `object` | no | — |
| `workflowName` | body | `string` | no | Optionally name your workflow |
