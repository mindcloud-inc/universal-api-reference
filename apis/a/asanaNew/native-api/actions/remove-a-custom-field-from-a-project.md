# Remove a custom field from a project with Asana

Removes a custom field from a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/removeCustomFieldSetting`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a custom field from a project](https://developers.asana.com/reference/removecustomfieldsettingforproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.custom_field` | body | `string` | yes |
| `project_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
