# Create Field with Laposta

Creates a custom field in Laposta.

## Endpoint

- **Method:** `POST`
- **Path:** `/field`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Create Field](https://api.laposta.nl/doc/index.en.php#fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | The ID of the list that will own the field. |
| `name` | body | `string` | yes | Field name. |
| `defaultvalue` | body | `string` | no | Default field value. |
| `datatype` | body | `list` | yes | Supported simple field type. Accepted values: `date`, `numeric`, `text`. |
| `required` | body | `boolean` | yes | Whether the field is required. |
| `in_form` | body | `boolean` | yes | Whether the field appears in the signup form. |
| `in_list` | body | `boolean` | yes | Whether the field is visible in the Laposta overview. |
