# Add a custom field to a project with Asana

Adds a custom field to a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/addCustomFieldSetting`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a custom field to a project](https://developers.asana.com/reference/addcustomfieldsettingforproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.custom_field` | body | `string` | yes |
| `data.insert_after` | body | `string` | yes |
| `data.insert_before` | body | `string` | yes |
| `data.is_important` | body | `boolean` | yes |
| `project_gid` | path | `string` | yes |
