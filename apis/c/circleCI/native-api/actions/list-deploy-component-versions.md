# List Deploy Component Versions with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/components/:component_id/versions`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Deploy Component Versions](https://circleci.com/docs/api/v2/#tag/Deploy/operation/listComponentVersions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_id` | path | `string` | no | The deploy component ID. |
