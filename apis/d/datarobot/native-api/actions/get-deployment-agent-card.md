# Get Deployment Agent Card with Datarobot

Retrieves the agent card for a deployment from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/:deploymentId/agentCard/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [Get Deployment Agent Card](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploymentId` | path | `string` | yes | The unique identifier of the deployment. |
