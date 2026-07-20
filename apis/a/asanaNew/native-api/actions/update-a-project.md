# Update a project with Asana

Updates a project in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:project_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a project](https://developers.asana.com/reference/updateproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `project_gid` | path | `string` | yes | Path parameter: project_gid |
| `data` | body | `object` | yes | — |
