# Update a custom field with Asana

Updates a custom field in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `custom_fields/:custom_field_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a custom field](https://developers.asana.com/reference/updatecustomfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_gid` | path | `string` | yes | Asana custom field gid parameter. |
| `data` | body | `string` | no | — |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
