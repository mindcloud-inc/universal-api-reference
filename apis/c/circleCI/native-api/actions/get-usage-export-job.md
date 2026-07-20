# Get Usage Export Job with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/usage_export_job/:usage_export_job_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Usage Export Job](https://circleci.com/docs/api/v2/#tag/Billing/operation/getUsageExport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | The CircleCI organization UUID. |
| `usage_export_job_id` | path | `string` | no | The usage export job UUID. |
