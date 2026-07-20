# Rollback Deployment with DeployHQ

Rolls back a deployment in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/deployments/:id/rollback`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Rollback Deployment](https://api.deployhq.com/docs#tag/Deployments/operation/rollbackProjectDeployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the deployment to rollback. |
| `mode` | body | `string` | no | Set to preview to preview the rollback or queue to execute immediately. Defaults to queue in DeployHQ. |
| `copy_config_files` | body | `boolean` | no | Whether to copy config files during rollback. DeployHQ defaults this to true. |
| `run_build_commands` | body | `boolean` | no | Whether to run build commands during rollback. DeployHQ defaults this to true. |
