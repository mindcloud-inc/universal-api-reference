# Create Organization Group with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:org_id/groups`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Organization Group](https://circleci.com/docs/api/v2/#tag/Groups/operation/createOrganizationGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The group description. |
| `name` | body | `string` | yes | The group name. |
| `org_id` | path | `string` | yes | The CircleCI organization UUID. |
