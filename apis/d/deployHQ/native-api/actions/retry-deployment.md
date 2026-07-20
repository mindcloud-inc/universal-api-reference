# Retry Deployment with DeployHQ

Retries an existing deployment in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/deployments/:id/retry`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Retry Deployment](https://api.deployhq.com/docs#tag/Deployments/operation/retryProjectDeploymentRetry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the deployment to retry. |
