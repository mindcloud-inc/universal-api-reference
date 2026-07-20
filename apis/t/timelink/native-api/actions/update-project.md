# Update Project with Timelink

Updates an existing project in Timelink.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Project](https://api.timelink.io/documentation#/Projects/patch_api_v1_projects__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
