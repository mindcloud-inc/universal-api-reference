# List Registered Model Version Deployments with Datarobot

Retrieves deployments for a registered model version from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/registeredModels/:registeredModelId/versions/:versionId/deployments/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [List Registered Model Version Deployments](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `registeredModelId` | path | `string` | yes |
| `versionId` | path | `string` | yes |
