# List Deployments with DeployHQ

Retrieves deployments for a project from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/deployments`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [List Deployments](https://api.deployhq.com/docs#tag/Deployments/operation/listProjectDeployments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `currently_running` | query | `boolean` | no | Filter to currently running deployments. Set to 1 to enable. |
| `to` | query | `string` | no | Filter deployments by parent identifier. |
