# Remove users from a project with Asana

Removes users from a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/removeMembers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove users from a project](https://developers.asana.com/reference/removemembersforproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.members` | body | `string` | yes |
| `project_gid` | path | `string` | yes |
