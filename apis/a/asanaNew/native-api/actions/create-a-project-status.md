# Create a project status with Asana

Creates a project status in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/project_statuses`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a project status](https://developers.asana.com/reference/createprojectstatusforproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `project_gid` | path | `string` | yes | Path parameter: project_gid |
| `data` | body | `object` | yes | — |
