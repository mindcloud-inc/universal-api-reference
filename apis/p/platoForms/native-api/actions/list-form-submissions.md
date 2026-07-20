# List Form Submissions with PlatoForms

Retrieves form submission metadata from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/{{form_identifier}}/submissions/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [List Form Submissions](https://apidocs.platoforms.com/#operation/form_submissions_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `sort` | query | `string` | no | Sort order (e.g., '-id' for newest first, '-submitted_date' for latest submissions) |
| `keywords` | query | `string` | no | Search keywords across searchable fields |
| `page` | query | `number` | no | Page number for pagination |
| `results_per_page` | query | `number` | no | Number of results per page |
