# Add followers to a project with Asana

Adds followers to a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/addFollowers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add followers to a project](https://developers.asana.com/reference/addfollowersforproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.followers` | body | `string` | yes | — |
| `opt_fields[]` | query | `array<string>` | no | — |
| `project_gid` | path | `string` | yes | Path parameter: project_gid |
| `data` | body | `object` | yes | — |
