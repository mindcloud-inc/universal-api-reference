# Update a section with Asana

Updates a section in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `sections/:section_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a section](https://developers.asana.com/reference/updatesection)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.insert_after` | body | `string` | yes |
| `data.insert_before` | body | `string` | yes |
| `data.name` | body | `string` | yes |
| `section_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
