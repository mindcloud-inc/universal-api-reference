# List Use Case Deployments with Datarobot

Retrieves deployments for a use case from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/useCases/:useCaseId/deployments/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [List Use Case Deployments](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `useCaseId` | path | `string` | yes | The ID of the use case. |
