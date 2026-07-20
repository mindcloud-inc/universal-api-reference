# List Organization Groups with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/groups`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Organization Groups](https://circleci.com/docs/api/v2/#tag/Groups/operation/getOrganizationGroups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | The CircleCI organization UUID. |
