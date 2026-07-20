# Get Pipeline Config with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/pipeline/:pipeline_id/config`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Pipeline Config](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineConfigById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `string` | no | Opaque pipeline identifier. |
