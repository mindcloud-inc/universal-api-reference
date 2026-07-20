# Create an enum option with Asana

Creates an enum option in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `custom_fields/:custom_field_gid/enum_options`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create an enum option](https://developers.asana.com/reference/createenumoptionforcustomfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_gid` | path | `string` | yes | Path parameter: custom_field_gid |
| `opt_fields[]` | query | `array<string>` | no | — |
| `data` | body | `object` | no | — |
