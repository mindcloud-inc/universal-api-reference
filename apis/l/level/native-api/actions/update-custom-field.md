# Update Custom Field with Level

Updates an existing custom field in Level.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/custom_fields/{id}`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Update Custom Field](https://levelapi.readme.io/reference/updatecustomfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the custom field. |
| `name` | body | `string` | no | The updated name of the custom field. |
| `admin_only` | body | `boolean` | no | Whether only administrators can view or edit this field. |
