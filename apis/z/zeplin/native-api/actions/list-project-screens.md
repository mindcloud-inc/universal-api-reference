# List Project Screens with Zeplin

Retrieves a list of project screens from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Screens](https://docs.zeplin.dev/reference/getprojectscreens)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `section_id` | query | `string` | no | Filter by section id |
| `sort` | query | `string` | no | Sort screens by their `section` or their `created` date |
