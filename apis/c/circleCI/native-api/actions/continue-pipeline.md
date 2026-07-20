# Continue Pipeline with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/pipeline/continue`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Continue Pipeline](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/continuePipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configuration` | body | `string` | no | Generated CircleCI configuration to continue with. |
| `continuation-key` | body | `string` | no | Continuation key returned by a setup pipeline. |
| `parameters` | body | `string` | no | Pipeline parameters for the continued pipeline. |
