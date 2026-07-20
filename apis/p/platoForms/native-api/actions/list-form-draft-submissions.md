# List Form Draft Submissions with PlatoForms

Retrieves draft form submissions from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/{{form_identifier}}/submissions/draft/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [List Form Draft Submissions](https://apidocs.platoforms.com/#operation/form_submissions_draft_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `sort` | query | `string` | no | Sort order (e.g., '-modified_date' for latest first) |
| `page` | query | `number` | no | Page number for pagination |
| `results_per_page` | query | `number` | no | Number of results per page |
