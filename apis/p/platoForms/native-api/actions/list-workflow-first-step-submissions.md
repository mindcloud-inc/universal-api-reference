# List Workflow First-Step Submissions with PlatoForms

Retrieves first-step workflow submissions from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow/{{workflow_identifier}}/submissions/ids/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [List Workflow First-Step Submissions](https://apidocs.platoforms.com/#operation/workflow_submissions_ids_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes | — |
| `sort` | query | `string` | no | Sort order ('-submitted_date' for newest first, 'submitted_date' for oldest) |
| `page` | query | `number` | no | Page number for pagination |
| `page_size` | query | `number` | no | Number of items per page (default: 50, max: 200) |
| `include_metadata` | query | `boolean` | no | Include submission metadata (date) - default: true |
