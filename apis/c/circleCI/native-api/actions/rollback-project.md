# Rollback Project with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/rollback`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Rollback Project](https://circleci.com/docs/api/v2/#tag/Rollback/operation/rollbackProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_name` | body | `string` | no | Component name to roll back. |
| `current_version` | body | `string` | no | Current deployed version. |
| `environment_name` | body | `string` | no | Environment name. |
| `namespace` | body | `string` | no | Deployment namespace. |
| `parameters` | body | `object` | no | Rollback parameters. |
| `project_id` | path | `string` | no | Opaque project identifier. |
| `reason` | body | `string` | no | Reason for the rollback. |
| `target_version` | body | `string` | no | Target rollback version. |
