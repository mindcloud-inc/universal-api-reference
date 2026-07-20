# List Engine Rules with Dremio

Retrieves engine rules from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/rules`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [List Engine Rules](https://docs.dremio.com/dremio-cloud/api/rules/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
