# Get Deploy Environment with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/environments/:environment_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Deploy Environment](https://circleci.com/docs/api/v2/#tag/Deploy/operation/getEnvironment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | no | The deploy environment UUID. |
