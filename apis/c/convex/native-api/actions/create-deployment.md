# Create Deployment with Convex

Creates a new deployment in Convex.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/create_deployment`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Create Deployment](https://docs.convex.dev/management-api/create-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Convex project ID. |
| `type` | body | `string` | yes | The deployment type to create. |
