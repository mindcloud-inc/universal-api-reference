# Reorder a custom field's enum with Asana

Reorders a custom field's enum options in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `custom_fields/:custom_field_gid/enum_options/insert`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Reorder a custom field's enum](https://developers.asana.com/reference/insertenumoptionforcustomfield)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_field_gid` | path | `string` | yes |
| `data.after_enum_option` | body | `string` | no |
| `data.before_enum_option` | body | `string` | no |
| `data.enum_option` | body | `string` | no |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
