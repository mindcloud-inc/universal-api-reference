# Delete Form Invitation with PlatoForms

Deletes an existing form invitation from PlatoForms.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Delete Form Invitation](https://apidocs.platoforms.com/#operation/invitation_prefill_form_delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes |
| `invitation_identifier` | path | `string` | yes |
