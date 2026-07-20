# Create Usage Export Job with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:org_id/usage_export_job`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Usage Export Job](https://circleci.com/docs/api/v2/#tag/Billing/operation/createUsageExport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | body | `string` | yes | The inclusive end date-time for the usage export. |
| `org_id` | path | `string` | yes | The CircleCI organization UUID. |
| `start` | body | `string` | yes | The inclusive start date-time for the usage export. |
