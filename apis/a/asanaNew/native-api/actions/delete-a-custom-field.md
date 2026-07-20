# Delete a custom field with Asana

Deletes a custom field from Asana.

## Endpoint

- **Method:** `DELETE`
- **Path:** `custom_fields/:custom_field_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Delete a custom field](https://developers.asana.com/reference/deletecustomfield)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_field_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
