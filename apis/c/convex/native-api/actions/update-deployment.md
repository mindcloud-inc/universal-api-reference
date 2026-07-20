# Update Deployment with Convex

Updates an existing deployment in Convex.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/deployments/:deployment_name`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Update Deployment](https://docs.convex.dev/management-api/update-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_name` | path | `string` | yes | The Convex deployment name. |
| `reference` | body | `string` | no | The deployment reference to set. |
| `sendLogsToClient` | body | `boolean` | no | Whether to send logs to the client. |
