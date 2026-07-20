# Create a Workflow with DocuPipe

Creates a workflow in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/on-submit-document`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Create a Workflow](https://docs.docupipe.ai/reference/post_workflow_on_submit_document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizeStep` | body | `object` | no | This step will always standardize the submitted document through one or more schemas you specify. |
| `standardizeReviewStep` | body | `object` | no | This step standardizes the document and immediately reviews every resulting standardization. |
| `classifyStandardizeStep` | body | `object` | no | This step allows you to decide on a list of class IDs to classify into, and define which schemas to standardize by, conditional on the classification result. You may choose to only standardize some of the classes, or standardize the same class by multiple schemas. |
| `splitStandardizeStep` | body | `object` | no | This step first runs a split operation on the submitted document, then standardizes every resulting sub-document using all schemas provided in `schemaIds`. |
| `splitClassifyStandardizeStep` | body | `object` | no | This step runs a split operation on the submitted document, then classifies each resulting sub-document, and finally standardizes any sub-document whose classification matches a provided class-to-schema mapping. |
| `workflowName` | body | `string` | no | Optionally name your workflow |
