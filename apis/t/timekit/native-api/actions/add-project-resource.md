# Add Project Resource with Timekit

Adds a resource to a project in Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id/resources`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Add Project Resource](https://developers.timekit.io/reference/add-resource-to-a-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `resource_id` | body | `string` | yes |
