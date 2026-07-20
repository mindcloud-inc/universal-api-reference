# Update Form Invitation with PlatoForms

Updates an existing form invitation in PlatoForms.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invitation/prefill/form/{{form_identifier}}/{{invitation_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Update Form Invitation](https://apidocs.platoforms.com/#operation/invitation_prefill_form_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes |
| `invitation_identifier` | path | `string` | yes |
