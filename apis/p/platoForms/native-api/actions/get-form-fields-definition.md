# Get Form Fields Definition with PlatoForms

Retrieves form field definitions from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/{{form_identifier}}/fields/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Get Form Fields Definition](https://apidocs.platoforms.com/#operation/form_fields_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `draft` | query | `boolean` | no | Get draft fields instead of published fields |
