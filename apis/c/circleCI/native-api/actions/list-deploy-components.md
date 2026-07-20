# List Deploy Components with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/components`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Deploy Components](https://circleci.com/docs/api/v2/#tag/Deploy/operation/listComponents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org-id` | query | `string` | yes | The CircleCI organization UUID. |
| `page-size` | query | `number` | yes | Number of records to return. |
