# Get Deployment with DeployHQ

Retrieves a deployment from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/deployments/:id`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Get Deployment](https://api.deployhq.com/docs#tag/Deployments/operation/getProjectDeploymentById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the deployment. |
