# Update Form Submission with PlatoForms

Updates an existing form submission in PlatoForms.

## Endpoint

- **Method:** `PUT`
- **Path:** `/submit/form/{{form_identifier}}/{{submission_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Update Form Submission](https://apidocs.platoforms.com/#operation/submit_form_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `submission_identifier` | path | `string` | yes | — |
| `submit_data[]` | body | `array<object>` | yes | — |
| `sync` | query | `boolean` | no | Wait for PDF generation before responding (not recommended for production) |
