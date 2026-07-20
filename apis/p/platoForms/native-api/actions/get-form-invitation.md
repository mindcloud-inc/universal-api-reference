# Get Form Invitation with PlatoForms

Retrieves form invitation details from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Get Form Invitation](https://apidocs.platoforms.com/#operation/invitation_prefill_form_read)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes |
| `invitation_identifier` | path | `string` | yes |
