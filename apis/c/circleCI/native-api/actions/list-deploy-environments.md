# List Deploy Environments with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/environments`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Deploy Environments](https://circleci.com/docs/api/v2/#tag/Deploy/operation/listEnvironments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org-id` | query | `string` | yes | The CircleCI organization UUID. |
| `page-size` | query | `number` | yes | Number of records to return. |
