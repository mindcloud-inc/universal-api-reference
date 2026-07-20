# Get Complete Workflow Chain with PlatoForms

Retrieves a complete workflow chain from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow/{{workflow_identifier}}/submission/{{submission_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Get Complete Workflow Chain](https://apidocs.platoforms.com/#operation/workflow_submission_read)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes |
| `submission_identifier` | path | `string` | yes |
