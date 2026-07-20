# Create Project with DeployHQ

Creates a new project in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Create Project](https://api.deployhq.com/docs#tag/Projects/operation/createProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `object` | yes | Project payload. DeployHQ accepts fields such as name, keypair_identifier, zone_id, and template_id. |
