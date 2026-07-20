# Delete Organization Group with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:org_id/groups/:group_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Organization Group](https://circleci.com/docs/api/v2/#tag/Groups/operation/deleteGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | no | The CircleCI group UUID. |
| `org_id` | path | `string` | no | The CircleCI organization UUID. |
