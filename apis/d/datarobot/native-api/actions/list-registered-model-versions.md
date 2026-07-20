# List Registered Model Versions with Datarobot

Retrieves versions for a registered model from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/registeredModels/:registeredModelId/versions/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [List Registered Model Versions](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registeredModelId` | path | `string` | yes | The ID of the registered model. |
