# Submit Form with PlatoForms

Creates a new form submission in PlatoForms.

## Endpoint

- **Method:** `POST`
- **Path:** `/submit/form/{{form_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Submit Form](https://apidocs.platoforms.com/#operation/submit_form_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `submit_data[]` | body | `array<object>` | yes | — |
| `sync` | query | `boolean` | no | Wait for PDF generation before responding (not recommended for production) |
