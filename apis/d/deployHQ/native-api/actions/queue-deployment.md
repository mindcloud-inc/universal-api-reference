# Queue Deployment with DeployHQ

Creates a deployment for a project in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/deployments`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Queue Deployment](https://api.deployhq.com/docs#tag/Deployments/operation/createProjectDeployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `deployment` | body | `object` | yes | Deployment payload. DeployHQ accepts fields such as branch, mode, start_revision, end_revision, parent_identifier, server_identifier, run_build_commands, use_latest, and skip_if_not_changes. |
| `schedule` | body | `object` | no | Optional schedule payload for future, daily, weekly, monthly, or custom deployment scheduling. |
