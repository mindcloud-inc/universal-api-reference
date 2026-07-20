# List Workflow Execution Trees with PlatoForms

Retrieves workflow execution trees from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow/{{workflow_identifier}}/trees/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [List Workflow Execution Trees](https://apidocs.platoforms.com/#operation/workflow_trees_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes | — |
| `page` | query | `number` | no | Page number |
| `results_per_page` | query | `number` | no | Items per page (max 100) |
| `status` | query | `string` | no | Filter by completion status |
| `sort` | query | `string` | no | Sort order |
