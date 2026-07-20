# Update project with Neon

Updates a project in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update project](https://api-docs.neon.tech/reference/updateproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `project` | body | `object` | yes | Neon API parameter project |
