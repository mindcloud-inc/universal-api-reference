# Create Form Invitation with PlatoForms

Creates a new form invitation in PlatoForms.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitation/prefill/form/{{form_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Create Form Invitation](https://apidocs.platoforms.com/#operation/invitation_prefill_form_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `invitation_name` | body | `string` | no | Name for the invitation (optional) |
| `invitation_url_number` | body | `number` | no | Number of invitation URLs to generate (max: 100) |
| `prefilled_data` | body | `object` | no | Pre-filled form data |
| `prefilled_field_state` | body | `object` | no | Field visibility and read-only states |
| `email_invitation` | body | `object` | no | — |
