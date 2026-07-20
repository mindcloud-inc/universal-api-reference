# List Registered Model Deployments with Datarobot

Retrieves deployments for a registered model from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/registeredModels/:registeredModelId/deployments/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [List Registered Model Deployments](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registeredModelId` | path | `string` | yes | The ID of the registered model. |
