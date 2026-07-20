# List Form Webhooks with PlatoForms

Retrieves webhooks for a form from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/form/{{form_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [List Form Webhooks](https://apidocs.platoforms.com/#operation/webhooks_form_read)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes |
