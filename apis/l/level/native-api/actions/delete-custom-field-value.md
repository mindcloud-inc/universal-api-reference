# Delete Custom Field Value with Level

Deletes a custom field value from Level.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/custom_field_values`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Delete Custom Field Value](https://levelapi.readme.io/reference/deletecustomfieldvalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_id` | body | `string` | yes | The ID of the custom field whose value should be deleted. |
| `assigned_to_id` | body | `string` | no | The ID of the device or group whose custom field value should be deleted. |
| `force` | body | `boolean` | no | Whether to delete descendant values as well. |
