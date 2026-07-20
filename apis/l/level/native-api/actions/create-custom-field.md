# Create Custom Field with Level

Creates a new custom field in Level.

## Endpoint

- **Method:** `POST`
- **Path:** `/custom_fields`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Create Custom Field](https://levelapi.readme.io/reference/createcustomfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the custom field. |
| `admin_only` | body | `boolean` | no | Whether only administrators can view or edit this field. |
