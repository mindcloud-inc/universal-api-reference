# Update Project with DeployHQ

Updates an existing project in DeployHQ.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:id`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Update Project](https://api.deployhq.com/docs#tag/Projects/operation/updateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier or permalink of the project. |
| `project` | body | `object` | yes | Project settings payload. DeployHQ accepts fields such as name, keypair_identifier, zone_id, and template_id. |
