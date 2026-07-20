# Create Project with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/:org_slug_or_id/project`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Project](https://circleci.com/docs/api/v2/#tag/Project/operation/createProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Project name. |
| `org_slug_or_id` | path | `string` | no | Organization slug or UUID. |
