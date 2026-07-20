# Submit Workflow Step with PlatoForms

Creates a workflow step submission in PlatoForms.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/submit/{{workflow_identifier}}/{{previous_submission_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Submit Workflow Step](https://apidocs.platoforms.com/#operation/workflow_submit_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes | — |
| `previous_submission_identifier` | path | `string` | yes | — |
| `submit_data[]` | body | `array<object>` | yes | Array of form field submissions |
| `sync` | query | `boolean` | no | Wait for PDF generation before responding (not recommended) |
