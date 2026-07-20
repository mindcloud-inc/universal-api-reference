# List Deployment Custom Metrics with Datarobot

Retrieves custom metrics for a deployment from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/:deploymentId/customMetrics/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [List Deployment Custom Metrics](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploymentId` | path | `string` | yes | The unique identifier of the deployment. |
