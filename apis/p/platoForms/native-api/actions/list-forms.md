# List Forms with PlatoForms

Retrieves a list of forms from PlatoForms.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [List Forms](https://apidocs.platoforms.com/#operation/forms_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter forms by status: published (default), draft, archived, or all |
