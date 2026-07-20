# Update Custom Field Value with Level

Updates a custom field value in Level.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/custom_field_values`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Update Custom Field Value](https://levelapi.readme.io/reference/updatecustomfieldvalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_id` | body | `string` | yes | The ID of the custom field to set the value for. |
| `assigned_to_id` | body | `string` | no | The ID of the device or group to assign the value to. |
| `value` | body | `string` | yes | The custom field value to set. |
| `force` | body | `boolean` | no | Whether to override descendant values when setting this custom field value. |
