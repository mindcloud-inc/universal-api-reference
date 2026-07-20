# Delete a project with Asana

Deletes a project from Asana.

## Endpoint

- **Method:** `DELETE`
- **Path:** `projects/:project_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Delete a project](https://developers.asana.com/reference/deleteproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_gid` | path | `string` | yes | Asana project gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
