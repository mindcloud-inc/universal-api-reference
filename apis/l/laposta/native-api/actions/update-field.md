# Update Field with Laposta

Updates an existing custom field in Laposta.

## Endpoint

- **Method:** `POST`
- **Path:** `/field/:fieldId`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Update Field](https://api.laposta.nl/doc/index.en.php#fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldId` | path | `string` | yes | The ID of the field to update. |
| `list_id` | body | `string` | yes | The ID of the list that owns the field. |
| `name` | body | `string` | no | Updated field name. |
| `defaultvalue` | body | `string` | no | Updated default field value. |
| `datatype` | body | `list` | no | Updated supported simple field type. Accepted values: `date`, `numeric`, `text`. |
| `required` | body | `boolean` | no | Whether the field is required. |
| `in_form` | body | `boolean` | no | Whether the field appears in the signup form. |
| `in_list` | body | `boolean` | no | Whether the field is visible in the Laposta overview. |
