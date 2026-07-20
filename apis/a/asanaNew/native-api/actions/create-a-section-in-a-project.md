# Create a section in a project with Asana

Creates a section in a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/sections`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a section in a project](https://developers.asana.com/reference/createsectionforproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.insert_after` | body | `string` | no |
| `data.insert_before` | body | `string` | no |
| `data.name` | body | `string` | yes |
| `project_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
