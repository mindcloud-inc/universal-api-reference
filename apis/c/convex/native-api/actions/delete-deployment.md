# Delete Deployment with Convex

Deletes an existing deployment from Convex.

## Endpoint

- **Method:** `POST`
- **Path:** `/deployments/:deployment_name/delete`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Delete Deployment](https://docs.convex.dev/management-api/delete-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_name` | path | `string` | yes | The Convex deployment name. |
