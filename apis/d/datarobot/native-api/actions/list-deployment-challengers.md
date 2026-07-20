# List Deployment Challengers with Datarobot

Retrieves challenger models for a deployment from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/:deploymentId/challengers/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [List Deployment Challengers](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploymentId` | path | `string` | yes | The unique identifier of the deployment. |
