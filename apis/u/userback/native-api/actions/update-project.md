# Update Project with Userback

Updates a Userback project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/project/:id`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Update Project](https://docs.userback.io/reference/updateproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The project ID to update. |
| `name` | body | `string` | no | The updated project name. |
| `url` | body | `string` | no | The updated project URL. |
