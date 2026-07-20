# Get Pipeline with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/pipeline/:pipeline_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Pipeline](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `string` | no | The CircleCI pipeline UUID. |
