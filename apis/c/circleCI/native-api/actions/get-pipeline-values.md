# Get Pipeline Values with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/pipeline/:pipeline_id/values`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Pipeline Values](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineValuesById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `string` | no | Opaque pipeline identifier. |
