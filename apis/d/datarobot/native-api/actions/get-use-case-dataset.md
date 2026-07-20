# Get Use Case Dataset with Datarobot

Retrieves dataset details for a use case from Datarobot.

## Endpoint

- **Method:** `GET`
- **Path:** `/useCases/:useCaseId/datasets/:datasetId/`
- **Base URL:** `https://app.datarobot.com/api/v2`
- **Official documentation:** [Get Use Case Dataset](https://docs.datarobot.com/en/docs/api/reference/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetId` | path | `string` | yes |
| `useCaseId` | path | `string` | yes |
