# Add users to a project with Asana

Adds users to a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/addMembers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add users to a project](https://developers.asana.com/reference/addmembersforproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.members` | body | `string` | yes |
| `project_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
