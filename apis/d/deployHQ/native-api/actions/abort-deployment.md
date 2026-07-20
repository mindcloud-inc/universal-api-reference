# Abort Deployment with DeployHQ

Aborts a running deployment in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/deployments/:id/abort`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Abort Deployment](https://api.deployhq.com/docs#tag/Deployments/operation/abortProjectDeployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the deployment. |
