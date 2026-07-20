# Remove followers from a project with Asana

Removes followers from a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/removeFollowers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove followers from a project](https://developers.asana.com/reference/removefollowersforproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.followers` | body | `string` | yes | — |
| `project_gid` | path | `string` | yes | Asana project gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.followers` | body | `string` | yes | Asana followers parameter. |
