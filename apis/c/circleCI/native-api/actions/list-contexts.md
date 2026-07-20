# List Contexts with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/context`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Contexts](https://circleci.com/docs/api/v2/#tag/Context/operation/listContexts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner-id` | query | `string` | yes | The CircleCI organization ID. |
| `owner-type` | query | `string` | no | The CircleCI owner type. Use organization for cloud orgs. |
