# Find Deployment Logs with v0

Finds logs for a v0 deployment.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/deployments/:deploymentId/logs`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Find Deployment Logs](https://v0.app/docs/api/platform/reference/deployments/find-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploymentId` | path | `string` | yes | Use the canonical dpl_... deployment ID returned by Find Deployments, not the bare token from the inspector URL. |
| `since` | query | `number` | no | Use the nextSince value returned by this action when paginating. Live verification showed the API expects a 13-digit millisecond timestamp in practice. |
